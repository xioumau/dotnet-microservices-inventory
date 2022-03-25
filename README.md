No arquivo ```task.json``` logo abaixo de:
```c#
"problemMatcher": "$msCompile",
```
Adicione:
```c#
 "group": {
        "kind": "build",
        "isDefault": true
      },
```
Para que o browser não abra por padrão, no arquivo ```launch.json``` delete o trecho de código:
```c#
// Enable launching a web browser when ASP.NET Core starts. For more information: https://aka.ms/VSCode-CS-LaunchJson-WebBrowser
      "serverReadyAction": {
        "action": "openExternally",
        "pattern": "\\bNow listening on:\\s+(https?://\\S+)"
      },
```
Dentro do diretório ```Properties``` no arquivo ```launchSettings.json``` mude as portas, no meu caso ficou assim:
```bash
"applicationUrl": "https://localhost:5005;http://localhost:5004",
```

Para importar o [pacote](https://github.com/xioumau/dotnet-create-package) que fizemos:
```bash
dotnet add package Play.Common
```
