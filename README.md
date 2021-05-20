# RBX1_TECLADO

En el launch "fake_turtlebot.launch" se incluye la siguiente instrucción
```
<remap from="/cmd_vel" to="/turtle1/cmd_vel"/>
```
Se usa remap para unir el nodo de **"turtle1/cmd_vel"** al **"/cmd_vel"** del package arbotix, lo que se busca con esto es conectar el nodo **turtle_teleop_key** del package **turtlesim** con los nodos de arbotix y asi poder controlar el robot desde el teclado.

* Las siguientes instrucciones se corren en terminales diferentes, para comprobar que el remap se realizó de manera correcta.
```
1. $ roscore
2. $ roslaunch rbx1_bringup fake_turtlebot.launch
3. $ rosrun rviz rviz -d `rospack find rbx1_nav`/sim.rviz
4. $ rosrun turtlesim turtle_teleop_key
```
<!--En ROS noetic se presentó un error, el cual se solucionó modificando el archivo "fake_turtlebot.launch" como se especificó dentro del mismo-->
