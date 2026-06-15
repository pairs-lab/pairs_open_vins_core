# pairs_open_vins_core

**PAIRS OpenVINS core** metapackage. Runs the PAIRS UAV system with OpenVINS visual-inertial
state estimation (launch / config / calibration for several camera-IMU rigs).

The OpenVINS libraries (`ov_core`, `ov_eval`, `ov_init`, `ov_msckf`) are kept
under their upstream names (third-party, from the `ctu-mrs/open_vins` fork) and
provided as separate `.deb` packages — they are NOT renamed to `pairs_*`.

Component repositories are managed via `ros_packages/.gitman.yml` (`gitman install`).

## Branches
- `ros1` — ROS 1 Noetic (catkin)
- `ros2` — ROS 2 Jazzy (ament_cmake)

## License
BSD 3-Clause. Derived from the CTU-MRS `pairs_open_vins_core`; original copyright
retained in [LICENSE](LICENSE).