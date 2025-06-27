
# Static Analysis

### Static Analysis of both Android and IOS Applications

## Android Application Static Analysis

**How to pull an app from Open Gapps**

* To do this we need to have Gapps enabled on our genymotion emulator
* Once that's done drop into the shell via `adb shell`
* List the available packages and grep for the desired application package by

```bash
pm list packages | grep 'swiggy'
```

* In order to get the exact `base.apk` which is the application we need list the full path to the same by

```bash
pm path 'in.swiggy.android'
```

* now we can jump out of the shell on a new terminal and pull the application to the desired directory by

```bash
adb pul /data/app/~~UpfV0bhVGStOefhLMzj_BA==/in.swiggy.android-AUExyvueKdFOlwlKB4VjMQ==/base.apk
```