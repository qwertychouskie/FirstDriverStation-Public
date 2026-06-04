# Gamepad Support Matrix

The FIRST Driver Station uses SDL for gamepad support. Most common gamepads work without custom configuration, but support can vary by operating system, connection type, controller firmware, and whether the controller exposes a stable serial number. Note that only wired support is marked in this matrix. Wireless controller support is not tracked.

## Compatibility Notes

- **Supported**: The controller is expected to work normally on that platform.
- **Partial**: The controller is detected, but some features or connection modes may not work consistently.
- **Unsupported**: The controller is not expected to work on that platform.
- **Has SN?** indicates whether the Driver Station can identify individual controllers of the same model using a serial number or equivalent stable identifier. See [Gamepad Locking](GamepadLocking.md) for why this matters.
- VID/PID values can differ between firmware versions, and hardware revisions. Confirm the value shown by the Driver Station for the specific controller in use when troubleshooting.

## Matrix

| Name | VID/PID | Windows | macOS | Linux | Has SN? | Notes |
|---|---|---|---|---|---|---|
| PlayStation 5 DualSense | `054C:0CE6` | Supported | Supported | Supported | Yes |  |
| PlayStation 5 DualSense Edge | `054C:0DF2` | Supported | Supported | Supported | Yes |  |
| Xbox Series | `045E:0B12` | Supported | Supported | Supported | No | Rumble support is spotty. |
| Xbox Elite Series 2 | `045E:0B00` | Partial | Partial | Partial | No | Back buttons are not supported, and rumble support is spotty. |
| Nintendo Switch Pro | `057E:2009` | Supported | Supported | Supported | Yes |  |
| Nintendo Switch 2 Pro | `057E:2069` | Supported | Unsupported | Supported | Yes |  |
| Nintendo NSO N64 | `057E:2019` | Supported | Supported | Supported | Yes | Mappings are odd due to the awkward button layout. |
| Nintendo NSO GameCube | `057E:2073` | Supported | Unsupported | Supported | Yes |  |
| Steam Controller 2026 | `28DE:1106` | Supported | Supported | Supported | Yes |  |
| REV USB PS4 Compatible |  | Supported | Supported | Supported | No |  |
| PowerA Advantage Switch 2 | `20D6:A720` | Partial | Partial | Partial | No | Shows up as a joystick without gamepad mappings. |
