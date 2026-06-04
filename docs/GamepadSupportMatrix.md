# Gamepad Support Matrix

The FIRST Driver Station uses SDL for gamepad support. Most common gamepads work without custom configuration, but support can vary by operating system, connection type, controller firmware, and whether the controller exposes a stable serial number.

## Compatibility Notes

- **Supported**: The controller is expected to work normally on that platform.
- **Partial**: The controller is detected, but some features or connection modes may not work consistently.
- **Unsupported**: The controller is not expected to work on that platform.
- **Has SN?** indicates whether the Driver Station can identify individual controllers of the same model using a serial number or equivalent stable identifier. See [Gamepad Locking](GamepadLocking.md) for why this matters.
- VID/PID values can differ between USB, Bluetooth, firmware versions, and hardware revisions. Confirm the value shown by the Driver Station for the specific controller in use when troubleshooting.

## Matrix

| Name | VID/PID | Windows | macOS | Linux | Has SN? | Notes |
|---|---|---|---|---|---|---|
| PlayStation 5 DualSense Controller | `054C:0CE6` | Supported | Supported | Supported | Yes |  |
| Xbox Series Controller | `045E:0B12` | Supported | Supported | Supported | No |  |
| Nintendo Switch 2 Pro Controller | `057E:2069` | Supported | Unsupported | Supported | Yes |  |
