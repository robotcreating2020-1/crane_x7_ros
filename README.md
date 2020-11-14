# gripper_swing  
  
炭酸の入ったボトルを振る動作をするコード、ペットボトルを模した円柱のモデルを追加したブランチです。  
  
---

###  gazebo上でシミュレーションを行う場合
  
シミュレータを使う場合、授業と同じように以下のコードを実行します。  

```sh
roslaunch crane_x7_gazebo crane_x7_with_table.launch
```  
---

###  実機を使う場合  
  ？？？

---

   
## アームに炭酸の入ったボトルを振らせる  
  
crane_x7_examples下にあるbottle_pick.pyを実行します。  
  
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

