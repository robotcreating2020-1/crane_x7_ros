# gripper_swing  
  
炭酸の入ったボトルを振る動作をするコード、ペットボトルを模した円柱のモデルを追加したブランチです。  
  


#  動作環境 
  
以下の環境で動作確認を行っています。  
・ROS Melodic  
　・OS: Ubuntu 18.04.5 LTS  
　・ROS Distribution: Melodic Morenia 1.14.3  
　・Rviz 1.13.13  
　・Gazebo 9.0.0  
   
 ---
 
 
  
###  gazebo上でシミュレーションを行う場合
  
シミュレータを使う場合、授業と同じように以下のコードを実行します。  

```sh
roslaunch crane_x7_gazebo crane_x7_with_table.launch
```  
---

###  実機を使う場合  
  
 実機で動作を客員する場合、CRANE_X7からx軸向きに300mm、y軸向きに200mm離れたところにボトルを設置します。  
 　　
 次に制御信号ケーブルを接続した状態で次のコマンドを実行します。  
 ```sh
 sudo chmod 777 /dev/ttyUSB0  
 roslaunch crane_x7_control crane_x7_control.lanch  
 ```

---

   
## 実行方法  
  
CRANE_X7にボトルを振らせるコードです。  
ボトルを設置した後、crane_x7_examples下にあるbottle_pick.pyを実行します。  
  
```sh
rosrun crane_x7_examples bottle_pick.py 
```  
  
ボトルは(x,y) = (0.3,0.2)に準備します。  
アームがボトルをつかんだ後、ボトルを6回ほど振り、机に置きます。  
  
ボトルを振るジョイントはfor文の中で直接指定しているので、容易に変更可能です。(デフォルトでは0番と6番を指定)  
また、動かす角度も変えられます。(デフォルトでは0番を30度、6番を45度にしています。)  

gazebo上での動作は以下のようになります。  
<img src=https://github.com/robotcreating2020-1/images/blob/master/simplescreenrecorder-2020-11-02_21.42.24.gif width=500px />  

---
  
  
###  実機で確認したいこと
現在、使用を予定しているコカ・コーラ スリムボトルはちゃんとつかめるのか  
実際に振っている様子  
 →これによってボトルの初期位置、グリッパーの開閉角度、アームを振る際の角度などもろもろのパラメータを調整  
 
 67~72行目　ボトルを掴みに行く座標  
 75行目　ハンド閉じる角度  
 89,90行目　ボトルを降る角度  

---
