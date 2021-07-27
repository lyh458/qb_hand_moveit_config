# QB Softhand MoveIt! Config Package

The MoveIt! config package of [QB SOFTHAND RESEARCH](https://qbrobotics.com/products/qb-softhand-research/).

## Usage

**Controlled real qbhand with MoveIt!:**

- bringup qbhand

```bash
roslaunch qb_hand_control control.launch standalone:=true activate_on_initialization:=true device_name:=qbhand robot_namespace:=qbhand
```

- controlled with Moveit!

```bash
roslaunch qb_hand_moveit_config moveit_planning_execution.launch robot_namespace:=qbhand
```

**Visualization in RVIZ without gazebo:**

```bash
roslaunch qb_hand_moveit_config demo.launch
```

**Simulation with gazebo:**

```bash
TODO
```

## TODO

- [ ] gazebo simulation supported.
