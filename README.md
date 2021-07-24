# QB Softhand MoveIt! Config Package

The MoveIt! config package of [QB SOFTHAND RESEARCH](https://qbrobotics.com/products/qb-softhand-research/).

## Branch introduction

The default launch file [control.launch](https://bitbucket.org/qbrobotics/qbhand-ros/src/production-kinetic/qb_hand_control/launch/control.launch) in [qbhand_ros](https://bitbucket.org/qbrobotics/qbhand-ros/src/production-kinetic/) will include and start robot_description, joint_state_publisher, robot_state_publisher in default, which is not good to integrate with manipulator. So a new bringup file [qbhand_bringup.launch](https://github.com/lyh458/qb_hand_moveit_config/blob/seperated_bringup/launch/qbhand_bringup.launch) is created and used in this branch.

## Usage

### With the default launch file [control.launch](https://bitbucket.org/qbrobotics/qbhand-ros/src/production-kinetic/qb_hand_control/launch/control.launch) in [qbhand_ros](https://bitbucket.org/qbrobotics/qbhand-ros/src/production-kinetic/) to bringup qbhand. 

**Controlled real qbhand with MoveIt!:**

- bringup qbhand

```bash
roslaunch qb_hand_control control.launch standalone:=true activate_on_initialization:=true device_name:=qbhand
```

- controlled with Moveit!

```bash
roslaunch qb_hand_moveit_config moveit_planning_execution.launch
```

**Visualization in RVIZ without gazebo:**

```bash
roslaunch qb_hand_moveit_config demo.launch
```

### With the modified launch file [qbhand_bringup.launch](https://github.com/lyh458/qb_hand_moveit_config/blob/seperated_bringup/launch/qbhand_bringup.launch).

- all commands are integrated in one launch file, so bringup qbhand and use Moveit! with the following command:

```bash
roslaunch qb_hand_moveit_config moveit_planning_execution_seperated.launch 
```

## TODO

- [ ] gazebo simulation supported.
