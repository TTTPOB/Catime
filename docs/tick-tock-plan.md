# Tick-Tock Countdown Sound Plan

1. **Configuration**
   - Add a new boolean setting `CLOCK_TICK_SOUND` with default `FALSE`.
   - Provide a function `WriteConfigTickSound` to persist the setting.
   - Read and write the value in the config file, including default generation and generic key writer.

2. **User Interface**
   - Introduce a menu item to toggle the tick‑tock sound. The menu reflects the current state and stores changes via `WriteConfigTickSound`.

3. **Timer Behaviour**
   - When the setting is enabled and the countdown is running, play a tick‑tock beep every second using `Beep` with alternating frequencies.
   - Ensure no sound plays once the countdown finishes or in count‑up/current‑time modes.

4. **Integration**
   - Wire the new toggle into existing configuration loading and saving paths.
   - Update build tests to ensure the project still compiles.
