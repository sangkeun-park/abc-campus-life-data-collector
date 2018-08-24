# ABC Campus Life Data Collector

## Versions
### v2.0.2
* Apks
    * [Release](./release/kaist.iclab.abc-v2.0.2-release.apk)
* Bug fixes
    * Crash when UI transition during async UI update
* Changes
    * Handle more survey trigger/cancel event.

### v2.0.1
* Apks
    * [Debug](./debug/kaist.iclab.abc-v2.0.1-debug.apk)
    * [Release](./release/kaist.iclab.abc-v2.0.1-release.apk)
* Bug fixes
    * App crashes when going to **All Experiments** and **Experiments** for < Android API 24
    * In responding to a survey, a circular button keeps animating even when **not save** is selected.
    * Survey download fails frequently
    * Survey interval is incorrect when there is no survey before.
* Changes
    * Add confirmation dialog for dropout experiment.
* To do
    * Add string resources for Korean
    * Optimization by deleting unused resources and library.

### v2.0.0
* Apks
    * [Debug](./debug/kaist.iclab.abc-v2.0.0-debug.apk)
    * [Release](./release/kaist.iclab.abc-v2.0.0-release.apk)

### v1.0.3 Hotfix
* Apks
    * [Debug](./debug/kaist.iclab.abc-v1.0.3-HotFix-debug.apk)
    * [Release](./release/kaist.iclab.abc-v1.0.3-HotFix-release.apk)
* Bug fixes
    * Crash when starting a collector without any data selected

### v1.0.3
* Apks
    * [Debug](./debug/kaist.iclab.abc-v1.0.3-debug.apk)
    * [Release](./release/kaist.iclab.abc-v1.0.3-release.apk)
* Changes
    * Workers are now handled only non-main thread (with JobIntentService)
    * Code refactoring 
* Settings
    * Survey will be triggered after 20 min. + 20 flex min. from the time when you are into a sedentary state.

### v1.0.2
* Apks
    * [Debug](./debug/kaist.iclab.abc-v1.0.2-debug.apk)
    * [Release](./release/kaist.iclab.abc-v1.0.2-release.apk)
* Changes
    * WiFi is not enabled if a user currently turns off WiFi. WiFi scanning is performed only when a user turn on WiFi.
    * Data traffic tracking is performed only when a screen is on. 
    * A user allows to select data that he/she want to provide.
    * Add UI for checking statuses of data collectors.
* Bug fixes
    * Not upload notification data
    * WiFi, Ambient Sound, and Location data automatically collected.
       

### v1.0.1-HotFix
* [Debug](./debug/kaist.iclab.abc-v1.0.1-debug.apk)
    * Fix: ESM scheduled time field is set to zero.
    * (Maybe) Fix: ESM interval is not properly work. 

### v1.0.1 
* [Debug](./debug/kaist.iclab.abc-v1.0.1-debug.apk)
* [Release](./release/kaist.iclab.abc-v1.0.1-release.apk)


## How-To
To be added...