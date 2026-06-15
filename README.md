# pairs_open_vins_core

Metapackage that pulls together everything needed to run the PAIRS UAV stack with OpenVINS
visual-inertial odometry as its state-estimation source. It aggregates the upstream OpenVINS
estimator with the PAIRS glue packages (estimator plugin, odometry republisher, IMU filter)
so that camera + IMU data can drive the UAV's state estimator.

The component repositories are declared in `ros_packages/.gitman.yml` and fetched with
`gitman install`.

## Contents (bundled via gitman)
- `open_vins` — upstream OpenVINS visual-inertial estimator (`ov_core`, `ov_init`,
  `ov_msckf`, `ov_eval`). Kept under its upstream name and provided as separate `.deb`
  packages — NOT renamed to `pairs_*`.
- `pairs_open_vins_estimator_plugin` — exposes OpenVINS as a state estimator inside the PAIRS
  estimation manager.
- `pairs_vins_republisher` — republishes OpenVINS odometry into the frames/topics the PAIRS
  stack expects.
- `pairs_vins_imu_filter` — IMU pre-filtering for the VIO pipeline.

## Branches
- `ros1` — ROS 1 Noetic (catkin)
- `ros2` — ROS 2 Jazzy (ament_cmake)

## License
BSD 3-Clause. Derived from the CTU-MRS `pairs_open_vins_core`; original copyright
retained in [LICENSE](LICENSE).
