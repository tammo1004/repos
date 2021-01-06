# repos

+ [Windows 10](#Windows-10)
+ [WSL 2](#WSL-2)
+ [Python](#Python)

## Windows 10

## WSL 2

#### 1. PowerShell(관리자)

```
$ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

#### 2. 재부팅

#### 3. 가상 머신 플랫폼 옵션 사용(PowerShell 관리지)

```
$ dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

#### 4. 리눅스 커널 업데이트 패키지

https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

#### 5. 재부팅

#### 6. WSL2를 기본 버전으로 설정(PowerShell)

```
$ wsl --set-default-version 2
```

#### 7. 리눅스 배포판 설치(Microsoft 스토어)

> Ubuntu 20.04. LTS

#### 8. Ubuntu 20.04. LTS

> Enter new UNIX username, New password

```
$ sudo apt update && sudo apt upgrade
```

#### 9. 배포 버전을 WSL2로 설정

```
$ wsl --list --verbose
  NAME            STATE           VERSION
* Ubuntu-20.04    Stopped         2
$ wsl --set-default-version 2
```

#### 10. git

```
$ git --version
git version 2.25.1
```

#### 11. VS Code

> Windows에서 설치… →
> Extension: Remote-WSL, Remote-Containers, Docker →
> WSL에서… `$ code .`

#### 12. Windows Terminal(Microsoft 스토어)

```
"defaults":
        {
            // Put settings here that you want to apply to all profiles.
            "fontFace": "Consolas",
            "fontSize": 11
        },
        "list":
        [
            {
                "guid": "{07b52e3e-de2c-5db4-bd2d-ba144ed6c273}",
                "hidden": false,
                "name": "Ubuntu-20.04",
                "source": "Windows.Terminal.Wsl"
            },
            {
                // Make changes here to the cmd.exe profile.
                "guid": "{0caa0dad-35be-5f56-a8ff-afceee452369}",
                "name": "Anaconda Prompt",
                "commandline": "cmd.exe \"/K\" C:\\Users\\PC\\anaconda3\\Scripts\\activate.bat C:\\Users\\PC\\anaconda3",
                "startingDirectory" : "C:\\Users\\PC",
                "icon":"%USERPROFILE%\\Anaconda3\\Menu\\anaconda-navigator.ico",
                "hidden": false
            }
        ]
```

## Python

#### 1. .venv

```
$ python3 --version
Python 3.8.5
$ sudo apt update && sudo apt upgrade
$ sudo apt upgrade python3

$ sudo apt install python3-pip
$ sudo apt install python3-venv

$ mkdir helloPython && cd helloPython
$ python3 -m venv .venv
$ source .venv/bin/activate
(.venv) $ python -m pip install --upgrade pip
(.venv) $ pip install pep8
(.venv) $ pip install autopep8
(.venv) $ pip install pylint
(.venv) $ deactivate
```

#### 2. VS Code에서 연동

> Crl + Shift + P... Python: Select Interpreter… Python 3.8.5 64-bit

#### 3. VS Code에서 Python 테스트

> Extension: Python (ms-python.python) →
> print("Hello World") → Ctrl + F5
