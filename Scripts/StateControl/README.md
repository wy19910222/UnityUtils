#用法
1. 将StateController脚本挂在父节点上（可以在标题里输入个名字用于区分）
2. 将继承于BaseStateCtrl的脚本StateCtrlXXX挂在同一节点或者子节点上
3. 在StateCtrlXXX里“Controller”变量选择为步骤1里的StateController
4. 在StateController中新建状态（默认有两个状态，如果只需要两个状态就不需要新建）
5. 选中StateController里的某个状态
6. 更改StateCtrlXXX所控制的属性的值
7. 点击StateController里的“记录状态”按钮
8. 重复步骤4-6，遍历所有状态

游戏运行过程中，只要选中某个状态，StateCtrlXXX所控制的属性就会被赋值成之前记录的值。

#关联控制  
StateController可以控制其他其他控制器，当自身状态改变时可以改变其他控制器的状态。  
注意：谨慎循环控制，容易造成死递归。

#扩展  
想要控制别的属性，只要新建脚本，继承BaseStateCtrl并重写TargetValue就可以了。
