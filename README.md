# hostguard_service


This is Project HostGuard.

## Install requirements
bash ./scripts/install-requirements.sh

## Build

```
./rebuild.sh
```
then: 
```
sudo ./build/examples/example1
```
to see the trace_pipe:
```
sudo cat /sys/kernel/tracing/trace_pipe
```

## mysql config
Before running, you need to config your mysql server and create an account:
host = "tcp://127.0.0.1:3306",
user = "JiaHao",
password = "123",

## Debug
Before debug in vscode, the build folder `build` should exists.
for the first time, debug launch may fail because `sudo gdb` needs passwd, you could execute `sudo ifconfig` and input passwd in the vscode debug terminal, so that commands such as `sudo xx` in this terminal could get rid of passwd for a moment.
