# dyno_hsr_install

mkdir hsr_ws && cd hsr_ws

wstool init src https://github.com/samiamlabs/dyno_hsr_install/raw/master/dyno_hsr.rosinstall

cd src && wstool update -j8

cd .. && rosdep install --from-paths src -i -y

catkin_make

source devel/setup.bash
