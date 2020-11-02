# gripper_swing  
  
炭酸の入ったボトルを振る動作をするコード、ペットボトルを模した円柱のモデルを追加したブランチです。  
  
---

###　gazebo上でシミュレータを使う場合  
  
シミュレータを使う場合、授業と同じように以下のコードを実行します。  

```sh
roslaunch crane_x7_gazebo crane_x7_with_table.launch
```  
---

###  実機を使う場合  
  ？？？

---

   
## Run bottole_pick.py  
  
crane_x7_examples下にあるbottle_pick.pyを実行します。  
  
```sh
rosrun crane_x7_examples bottle_pick.py 
```  
  
ボトルは(x,y) = (0.3,0.2)に準備します。  
アームがボトルをつかんだ後、ボトルを6回ほど振り、机に置きます。  

---
