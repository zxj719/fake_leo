# fake_leo
connect raspberry with lidar
in ros2_ws/src
```bash
git clone -b ros2 https://github.com/Slamtec/rplidar_ros.git
cd ..
colcon build --symlink-install
source ./install/setup.bash
sudo chmod 777 /dev/ttyUSB0
cd src/rplidar_ros/
source scripts/create_udev_rules.sh
alias build="cd ~/ros2_ws;colcon build;source install/setup.bash"
```
new terminal
```bash
build
ros2 launch navigation navigation.launch.py
```

