# Patches

Patches applied on top of BASE.env. Each entry's `source` is an upstream URL pinned
to a commit, or `armada` if it's original; a URL source with no `notes` is verbatim.
`notes` mean the file was modified.

- `patches/0001-fix-gamepad-share-raw-input.patch`
  source: armada
- `patches/0002-fix-force-feedback-reset-effects-when-replacing-targets.patch`
  source: armada
- `patches/0004-fix-Hardware-Support-KONKR-Pocket-FIT-MCU-system-buttons.patch`
  source: armada
- `patches/0005-feat-ssc-qualcomm-sensor-core-support.patch`
  source: https://github.com/ShadowBlip/InputPlumber/pull/590/commits/3caa7902d92e49b86fed567df61a0677304ae8bf
  notes: Adds the FastRPCDevice.Id polkit action and the INPUTPLUMBER_FASTRPC opt-in, fixes scaling, polling, opening, library loading and sample rate, and moves the driver to the 0.83 pattern.
- `patches/0006-feat-ssc-gyro-auto-calibration.patch`
  source: armada
- `patches/0007-feat-ssc-device-enablement.patch`
  source: armada
- `patches/0008-feat-ssc-suspend-source-devices-across-system-sleep.patch`
  source: armada
- `patches/0009-fix-Hardware-Support-correct-face-button-mapping-for.patch`
  source: armada
  notes: The kernel reports face buttons by physical position on Nintendo-layout devices (A top-right as BTN_EAST, B bottom-right as BTN_SOUTH, X bottom-left as BTN_WEST, Y top-left as BTN_NORTH). Upstream swapped NORTH/WEST, which left A as B, B as A, X as Y and Y as X. The map now swaps the A and B sources; X and Y already line up with the Xbox layout. Verified on Retroid Pocket 5 and Pocket 6; the map is shared with Retroid Pocket Mini/Nova and AYN Odin 2/3.
