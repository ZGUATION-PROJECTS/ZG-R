# SuperMario Tweaker v3.0.1 - Snapdragon

### 🔄 Updates & Fixes
- Fix Bootloop Issues and SystemUI Crashes

# SuperMario Tweaker v3.0.0 - Snap

### 🔄 Updates & Fixes
- Now Support Android 9+
- Improve `action.sh` code
- Fix Status Bar Lags When Pull Down
- Reduce Module Size a Little
- Some Improvements and Fixes

### 🆕️Adds:
- Enabled Skia renderer for smoother UI.
- Reduced touch delay and improved response time.
- Disabled backpressure and caching to lower frame latency.
- Tuned graphics cache sizes for better performance.
- Forced GPU usage instead of CPU where possible.
- Boosted UI thread priority for faster animations.
- Enabled memory optimizations and disabled system logs.
- Applied general power-saving and fast boot tweaks.

# SuperMario Tweaker v2.3.0 - Changelog

### 🔄 Updates:
- Update Vulkan Version to `v25.1.3`
- Add `Clear Cache` at action button
- Readd old tweaks from `v2.0.1`
- Minimalistic installation UI
- New thumbnail
- Add `SuperMarioTweaker-Banner` and `SMTW-Banner.jpg` at one folder `assets`

### 🆕️ Adds:

### New Tweaks From La Flame:
- 🧠 Memory Management Tweaks
Optimizes memory usage by prioritizing important apps and allowing the system to kill unimportant background apps more aggressively.

- ⚙️ CPU Scheduling Tweaks
Reduces delays when switching apps and improves responsiveness by adjusting CPU-related behaviors.

- ☕ ART/Dalvik VM Tweaks
Enhances app performance by optimizing how the Android Runtime compiles and runs applications.

- 🖼️ Graphics & Rendering Tweaks
Improves graphics performance and increases frame rates (FPS) by disabling VSync and enabling faster rendering techniques.

- 📊 Profiler and Debugging Tweaks
Disables system profiling, logging, and debugging tools to reduce background load and improve privacy.

- 📦 Vendor-Specific Tweaks
Disables features like MemoryPlus that emulate virtual RAM, which may slow down devices that already have sufficient physical RAM.

<br />

# SuperMario Tweaker v2.2.0 - Changelog 

🔄Updates:
- Add `action button` to clear GPU cache
- Clean unnecessary tweaks in SuperMario-Tweaker.sh script
- Change how module work
- improvements here and there

🛠️Fixes:
- Touch & Input
  - Removed fine-tuned touch calibrations: pressure scaling, size scaling/bias, distance calibration and scaling.
  - Removed limits on multitouch event rate (windowsmgr.max_events_per_sec).
  - These affect touch sensitivity, accuracy, and UI responsiveness.

- GPU & Graphics:
  - Removed increased GPU buffer count (debug.egl.buffcount=4) which can improve frame buffering.
  - Removed several SurfaceFlinger optimizations like disabling crop recompute and backpressure.
  - Removed disabling of partial invalidates (debug.hwui.render_dirty_regions=false), impacting rendering efficiency.

- Vsync and Frame Sync:
  - Removed disabling of vsync (debug.hwui.disable_vsync=true and debug.cpurend.vsync=false) to reduce screen tearing and improve frame timing.
  - Removed swap interval tweaks (debug.egl.swapinterval=0 and debug.gr.swapinterval=0) affecting frame pacing.

- System Stability and Memory:
  - Removed disabling of killing resource-heavy tasks (debug.kill_allocating_task=0) which helps free memory.
  - Removed disabling process limit (ENFORCE_PROCESS_LIMIT=false), avoiding system overload.

- Visual Quality:
  - Removed disabling of dithering and MSAA forcing, which can degrade visual quality.

- Gaming & Display:
  - Removed disabling of Game Mode (persist.sys.game.turbo=0), potentially reducing gaming performance boosts.
  - Removed forced 120Hz refresh rate and dynamic FPS settings, which save battery but can limit smoothness.

# SuperMario Tweaker V2.1.0 - Changelog
- Delete unnecessary tweaks to fix bootloop for some devices
- Delete thermel controller and powerhint (Not needed anymore)
- Turnip (Vulkan driver) upgraded to Mesa 25.1.1, synced with latest upstream changes.
- Delete CPU & GPU spoofing to prevent bugs "especially with camera"
- Fixes here and there
- New Banner :)

# SuperMario Tweaker V2.0.1 - Changelog
- Delete wrong " from customize.sh to fix installation process

# SuperMario Tweaker V2.0.0 - Changelog

### Fixes & Updates
- Delete duplicated lines in system.prop
- Clean code (thanks to @ZG089)
- Delete DT module automatically if detected (thanks to @ZG089)
- Improved installation UI (thanks to @ZG089)
- Delete unnecessary audio, Dalvik, logging, and network tweaks
- Removed duplicate `build.prop` entries
- Reorganized tweaks for better structure
- Update update.json (to update module from root manager in next updates)
- Update Mesa Turnip to v25.1.0


## New Additions

### SuperMario-Tweaker.sh Script
- Full device idle mode and aggressive battery optimizations.
- System settings tuning (freeform windows, color enhancements).
- Dynamic Dalvik VM & HWUI adjustments based on RAM.
- App background restriction for bloatware and telemetry apps.
- System clean-up on execution (Dalvik cache wipe).

### Powerhint.xml Configurations
(This file is used to control CPU and memory performance for specific tasks, like using the camera or recording videos at different frame rates. It tells the system when to boost CPU speed, keep performance high, or optimize memory, to make sure everything runs smoothly.)

- Optimizations for 30FPS, 60FPS, and HFR video modes.
- CPU core scheduling and frequency boosting.
- Bandwidth and memory access optimizations.
- Target-specific tuning (bengal, scuba, khaje).

## Gaming Performance Enhancements
- CPU bandwidth control and high CPU frequency locking.
- Game Mode activation for boosted performance.
- Dynamic CPU, RAM, GPU frequency adjustments.
- Stable 120 FPS support and game rendering prioritization.
- Ultra and Balanced Performance Modes selectable.

## Performance Improvements
- Enabled high-performance CPU/GPU modes.
- App launch acceleration with usap_pool.

## Battery Optimizations
- Fine-tuned power-saving features.
- Sleep mode enhancements for radios and sensors.

## Display and Graphics Enhancements
- Forced GPU rendering and SurfaceFlinger tuning.
- Improved FPS, animation smoothness, and graphics acceleration.

## Game Mode and High FPS
- Locked display to 120Hz refresh for games.
- Disabled dynamic FPS scaling for stability.

## Touch and Input Optimizations
- Faster touch response and increased fling velocity.
- Improved calibration for touch accuracy.

## RAM and Memory Management
- Enabled zRAM compression.
- Adjusted cached apps limit for better multitasking.

## System Tweaks
- Faster app launches via IORAPD prefetching.
- Optimized background process handling.

## Snapdragon-Specific Enhancements
- Qualcomm display and rendering optimizations.
- Forced hardware acceleration.

## UI and Visual Smoothness
- OLED panel optimizations.
- Reduced frame drops and smoother animations.

## Hardware Composition Changes
- Enabled dynamic CPU-GPU composition.

## Stability and Performance Improvements
- Removed redundant logs and services.
- Improved RAM usage and responsiveness.
