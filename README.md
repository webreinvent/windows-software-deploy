# windows-software-deploy
- Open PowerShell as "Run as Administrator"
- Paste following and press enter:
```sh
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
or
```sh
Set-ExecutionPolicy Bypass -Scope Process -Force; `
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

- Set Cache Path
```sh
choco config set cacheLocation D:\Choco\softwares
```

- Use following command to install all softwares:
```sh
choco install Packages.config --yes
```
or

```sh
choco install Packages.config --yes --force
```
