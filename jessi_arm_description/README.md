# URDF for Jessi Arm
Robot description of Jessi Arm using xacro.
- Jessi Arm is 5 DoF manipulator
- There is five joints
- Gripper joint ignored


### Check .xacro files with check_urdf.
```bash
$ check_urdf <(xacro jessi_arm_robot.xacro)
robot name is: jessi_arm
---------- Successfully Parsed XML ---------------
root Link: world has 1 child(ren)
    child(1):  base_link
        child(1):  link1
            child(1):  link2
                child(1):  link3
                    child(1):  link4
                        child(1):  link5
```

### Use urdf_to_graphiz to visually check the .xacro.
```bash
$ urdf_to_graphiz <(xacro jessi_arm_robot.xacro)
Created file jessi_arm.gv
Created file jessi_arm.pdf
$ evince jessi_arm.pdf
```

### jessiarm.launch
```bash
roslaunch jessi_arm_description jessiarm.launch
```
<p align="center">
    <img src="../doc/joint_states.png" width="300" />
</p>

### launch rviz

```bash
rviz
```
<p align="center">
    <img src="../doc/rviz.png" width="400" />
</p>