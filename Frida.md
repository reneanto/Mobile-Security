
# Frida

## Install Client

*  On linux create a python virtual env by doing

```bash
python3 -m venv venv
```

* Then activate it by executing

```bash
source ./venv/bin/activate
```

*  Then install frida by pip

```bash
pip3 install frida-tools
```

## Install Server

* We're doing this on genymotion so get the arm64 based server

```bash
wget https://github.com/frida/frida/releases/download/17.2.4/frida-server-17.2.4-android-arm64.xz
```

* Un-archive it by 

```bash
xz -d frida-server-17.2.4-android-arm64.xz
```

*  Move it to the AVD and make it executable by following steps

```bash
adb root
adb push frida-server /data/tmp/local/
adb shell
su
cd /data/tmp/local
chmod 755 frida-server
```

* Start the server by

```bash
adb shell "/data/tmp/local/frida-server &"
```

*  To verify if the process has started or not

```
adb shell
ps | grep frida-server
```


* back on our client we can see the processes via listing out them by

```bash
frida-ps -U
```