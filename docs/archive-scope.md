# Archive scope

The project dates to the 2023 WRO Future Engineers season. The new overview and compact preview images were added during the portfolio update in 2026. The source files remain in their original directory, and the existing Git history is preserved.

## Files that survive

| File | Role in the archive |
|---|---|
| `manage.py` | DonkeyCar vehicle pipeline and driving entry point |
| `train.py` | Command-line wrapper around DonkeyCar's training pipeline |
| `calibrate.py` | DonkeyCar actuator-calibration utility |
| `config.py` | Saved framework settings, including camera and drivetrain selection |
| `myconfig.py` | Commented configuration template; no active overrides |
| `FEV001.ev3` | EV3 project file |

All five Python files parse successfully with a current Python interpreter. This checks syntax only; no motors were connected or vehicle-control entry points executed.

## Reproduction limits

The archive has no trained model and no complete training dataset. An exact DonkeyCar package version is not recorded. The team report mentions TensorFlow 2.9 compatibility work, but that alone does not pin the complete software environment.

The saved configuration uses `PWM_STEERING_THROTTLE`, while the report describes an EV3/Bluetooth vehicle. The original Python bridge for that integration has not been identified. The report also discusses additional sensors, which should not be assumed to be implemented by the saved framework configuration.

There is not enough evidence here to claim a measured lap-completion rate or inference latency. Driving footage demonstrates the prototype, not a controlled performance evaluation.

## Inspecting safely

Start by reading the configuration and project report. Running `manage.py` or `calibrate.py` can access hardware through DonkeyCar, so those scripts should be reviewed against the actual connected vehicle first. The EV3 file can be inspected in a compatible EV3 project editor.

This archive is useful for understanding the approach and development history. Reproducing the vehicle would require reconstructing the environment and checking its hardware interfaces.
