### Useful commands to enable/disable PAC file, and proxy

Check current settings
```
Get-Item "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings"
```

Set PAC file

```
Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "AutoConfigURL" -value "http://proxypac.domain.com/proxy.pac"
```
Enable/disable Proxy

```
Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "ProxyEnable" -value "1"
Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "ProxyEnable" -value "0"
Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "ProxyServer" -value ""
Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "ProxyServer" -value "http=127.0.0.1:8888;https=127.0.0.1:8888;ftp=127.0.0.1:8888"

Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "AutoConfigURL" -value $null
Set-ItemProperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Internet Settings" -name "ProxyServer" -value $null

```
