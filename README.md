# Board detection

Playback of the Overlapping multi camera sequence in the industrial calibration RViz view.

https://github.com/user-attachments/assets/c87b0f03-f9db-43ca-8430-fdb283b6c8a2

## What the video shows

- Left: `/image_annotated`, the 916 frames looping with the detected Charuco corners drawn on them.
- Center: `cal_target_frame` moving in front of a fixed camera as each frame is solved.

The board is the Seq02 5×5 Charuco target: 9.15 cm squares, `DICT_6X6_1000`, marker IDs starting at 144.

## Play it back

```bash
source /opt/ros/jazzy/setup.bash
source ~/workspace/industrial_calib/install/setup.bash
ros2 launch industrial_calibration_ros data_collection.launch.xml \
  config_file:=/path/to/target_detector_config.yaml
