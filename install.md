# Install OpenCode

## Windows Terminal
### via npm
```PowerShell
winget install OpenJS.NodeJS.LTS --silent --accept-package-agreements

$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")

npm i -g opencode-ai

powershell -NoExit -Command "Set-Location '$PWD'; Write-Host 'OpenCode installed successfully' -ForegroundColor Cyan" ; exit
```

### via Scoop
```PowerShell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

scoop install opencode
```
## IDE

### Antigravity
![alternate text](/assets/screenshot1.png)

Extensions > Search > Install

Extension ID `sst-dev.opencode`

Extension link: https://open-vsx.org/vscode/item?itemName=sst-dev.opencode

### VS Code
![alternate text](/assets/screenshot2.png)

Extensions > Search > Install

Extension ID `sst-dev.opencode`

Extension link: https://marketplace.visualstudio.com/items?itemName=sst-dev.opencode
