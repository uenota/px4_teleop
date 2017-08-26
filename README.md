# px4_teleop
PX4 teleop package

## Nodes
- px4_teleop_com  
  Teleop node with commands
- px4_teleop_joy  
  Teleop node with joystick
- joy_publisher  
  Publishes sensor_msgs::Joy message to /joy_publisher/joy topics

## Launch
- teleop_joy.launch  
  Runs px4_teleop_joy and joy_publisher
  
## Config
Config files contain axes and buttons mapping
- f710.yaml  
  For Logicool f710 joystick
- f310.yaml  
  For Logicool f310 joystick
- u3312s.yaml  
  For Elecom U3312S joystick

## Running Nodes
px4_teleop_joy node reads a config file written in yaml.  
Run the following command to read specific config file.  
```bash
roslaunch px4_teleop teleop_joy.launch joy_config_path:=<path_to_config>
```

In addition to this, an RC mode is set 1 by default.  
Run the following command to change the RC mode.  
```bash
roslaunch px4_teleop teleop_joy.launch joy_rc_mode:=<rc_mode>
```
