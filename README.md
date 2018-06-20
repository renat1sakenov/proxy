# proxy
An minimal authenticating HTTP(S) forward proxy based on https://github.com/adamfisk/LittleProxy. You can easily add sniffing / rewriting if needed. In short: Fiddler in Java 

# Installation on Windows
## Download the binary. 

```
powershell -Command "$proxy = [System.Net.WebRequest]::GetSystemWebProxy();$proxy.Credentials = [System.Net.CredentialCache]::DefaultCredentials;$wc = new-object system.net.WebClient;$wc.proxy = $proxy;$wc.DownloadFile('https://jitpack.io/com/github/baloise/proxy/-SNAPSHOT/proxy--SNAPSHOT.jar', '%USERPROFILE%/proxy.jar');"
```
You can look up the current jay version @ https://jitpack.io/com/github/baloise/jay/jay/-SNAPSHOT/maven-metadata.xml

## Create start up item
```
echo powershell -Command Start-Process 'javaw.exe' '-jar "%userprofile%\proxy.jar"' -NoNewWindow > "%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup\proxy.bat"
```

## Run
```
powershell -Command Start-Process 'javaw.exe' '-jar "%userprofile%\proxy.jar"' -NoNewWindow
```
