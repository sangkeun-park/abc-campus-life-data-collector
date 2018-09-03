# ABC Campus Life Data Collector

## Versions
### v2.0.8
* Apks: [Download](./debug/kaist.iclab.abc-v2.0.8-debug.apk)
* Bug fixes:
    * 재부팅 시 설문 전달 시간이 제대로 맞춰지지 않는 오류 해결
* Changes:
    * 다른 기기에서 이미 실험 중인 계정으로 접속했을 시 설문 전달 시간 등을 동기화 처리함
    * 또한, 사용자 권한이 필요한 데이터를 제공하기로 했으면 권한 설정을 알리는 안내 메시지를 출력

### v2.0.7
* Apks: [Download](./debug/kaist.iclab.abc-v2.0.7-debug.apk)
* Bug fixes:
    * 실험 기간이 지났음에도 실험이 종료되지 않는 오류 해결
    * 설문 전달이 정확한 타이밍이 가지 않는 오류 해결
* Changes
    * 설문 트리거 정책 변경
        * 초기 기간이 지나면 곧바로 알림이 전달되고, 이 후 정해진 시간 간격으로 전달됨
        * 만약 시간 단위를 일 (TimeUnit.DAYS)로 설정하면, 정확한 시간이 아닌 해당 일자를 의미
            * 예) 현재 시간이 9월 2일 18시 일 때, 이틀 뒤 ```SurveyTime(value = 2, TimeUnit.DAYS)``` 는 9월 4일 00시를 의미.
        * 정확하게 시간을 정하고 싶을 때는 TimeUnit.DAYS 보다 작은 시간 단위를 사용
            * 예) 현재 시간이 9월 2일 18시 일 때, 48시간 후 ```SurveyTime(value = 48, TimeUnit.HOURS)```로 설정하면 9월 4일 18시를 의미. 
        

### v2.0.6
* Apks: [Download](./debug/kaist.iclab.abc-v2.0.6-debug.apk)
* Bug fixes:
    * 미응답 알림이 계속 오는 오류 해결.
    
### v2.0.5
* Apks: [Download](./debug/kaist.iclab.abc-v2.0.5-debug.apk)
* Bug fixes:
    * Android API 22 에서 설문 저장 시도 시 크래쉬 나는 문제 해결.

### v2.0.4
* Apks: [Download](./debug/kaist.iclab.abc-v2.0.4-debug.apk)
* Bug fixes:
    * 마지막 동기화 시간이 제대로 업데이트 되지 않는 버그.
* Changes
    1. API 23 (v6.0.0) 부터 Android Doze mode 가 적용됨에 따라, JobScheduler 및 Worker 가 제대로 동작하지 않음.
        1. 이에 대응하기 위하여, 설문 알림은 AlarmManager.setExactAndWhileAllowIdle 으로 변경함.
    2. 내부적인 Exception 은 ABCException 클래스를 상속함.
    3. Drawer 에서 현재 앱 버전, 실험 참여 상태 등을 확인 할 수 있음.

### v2.0.3
* Apks: [Download](./debug/kaist.iclab.abc-v2.0.3-debug.apk)
* Bug fixes:
    1. 설문 저장을 했음에도 다시 수정을 할 수 있는 버그
    2. 설문 저장 이후 다시 설문을 열었을  때 이전 응답이 제대로 표시되지 않는 버그
    3. 설문 리스트 목록이 실시간으로 업데이트 되지 않는 버그
* Changes
    1. 디버그 목적을 위하여 백그라운드에서 수행 되고 있는 프로세스를 서버에 업로드 하도록 변경.

### v2.0.2-HotFix-1
* Apks
    * [Download](./release/kaist.iclab.abc-v2.0.2-HotFix-1-release.apk)
* Bug fixes
    * Cannot parse survey
        * Error in Android Kotlin Library v1.2.60.   

### v2.0.2
* Apks
    * [Download](./release/kaist.iclab.abc-v2.0.2-release.apk)
* Bug fixes
    * Crash when UI transition during async UI update
* Changes
    * Handle more survey trigger/cancel event.

### v2.0.1
* Apks
    * [Download](./debug/kaist.iclab.abc-v2.0.1-debug.apk)
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
    * [Download](./debug/kaist.iclab.abc-v2.0.0-debug.apk)

### v1.0.3 Hotfix
* Apks
    * [Download](./debug/kaist.iclab.abc-v1.0.3-HotFix-debug.apk)
* Bug fixes
    * Crash when starting a collector without any data selected

### v1.0.3
* Apks
    * [Download](./debug/kaist.iclab.abc-v1.0.3-debug.apk)
* Changes
    * Workers are now handled only non-main thread (with JobIntentService)
    * Code refactoring 
* Settings
    * Survey will be triggered after 20 min. + 20 flex min. from the time when you are into a sedentary state.

### v1.0.2
* Apks
    * [Download](./debug/kaist.iclab.abc-v1.0.2-debug.apk)
* Changes
    * WiFi is not enabled if a user currently turns off WiFi. WiFi scanning is performed only when a user turn on WiFi.
    * Data traffic tracking is performed only when a screen is on. 
    * A user allows to select data that he/she want to provide.
    * Add UI for checking statuses of data collectors.
* Bug fixes
    * Not upload notification data
    * WiFi, Ambient Sound, and Location data automatically collected.
       

### v1.0.1-HotFix
* [Download](./debug/kaist.iclab.abc-v1.0.1-debug.apk)
    * Fix: ESM scheduled time field is set to zero.
    * (Maybe) Fix: ESM interval is not properly work. 

### v1.0.1 
* [Download](./debug/kaist.iclab.abc-v1.0.1-debug.apk)

## How-To
To be added...