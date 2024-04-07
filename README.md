![AutoGeaconC2](https://socialify.git.ci/TryGOTry/AutoGeaconC2/image?description=1&forks=1&issues=1&language=1&name=1&owner=1&stargazers=1&theme=Light)
# AutoGeaconC2

为了方便脚本小子的工具：一键读取Profile自动化生成geacon实现跨平台上线CobaltStrike

Ps：为了增加分析成本，本项目不准备开源。

已适配大量profile配置，如遇到问题，请提交issues！

已适配猫猫cs,以及cdn上线.
# How To Use
1.下载releases中的AutoGeaconC2.cna，然后在cs客户端中导入cna

2.在服务端下载releases中根据系统下载AutoGeaconC2

3.下载releases中的BeaconTool.jar用于生成rsa的key。 java -jar BeaconTool.jar -i .cobaltstrike.beacon_keys

4.把上面生成的rsa的key填入AutoGeaconC2中生成Geacon客户端
```
AutoGeaconC2.exe -rsa "xxx" -profile c.profile -u https://127.0.0.1
```

## CobaltStrike Commands
已实现的功能如下
```shell
1.命令执行 执行shell version 查看当前客户端版本
2.文件管理(查看,上传,下载)
3.Sleep
4.Cd
5.Mkdir
6.Pwd
7.Cp
8.Mv
9.tasklit
10.spawn 执行shell spawn  需要当前进程文件存在.spawn上来的进程名中会包含(fork)
```
## Usage

```shell
                _         _____                             _____ ___  
     /\        | |       / ____|                           / ____|__ \ 
    /  \  _   _| |_ ___ | |  __  ___  __ _  ___ ___  _ __ | |       ) |
   / /\ \| | | | __/ _ \| | |_ |/ _ \/ _` |/ __/ _ \| '_ \| |      / / 
  / ____ \ |_| | || (_) | |__| |  __/ (_| | (_| (_) | | | | |____ / /_ 
 /_/    \_\__,_|\__\___/ \_____|\___|\__,_|\___\___/|_| |_|\_____|____|
                                                                       

Usage:
  # 是否运行后自删除，开启后无法执行spawn命令
  -delete
        DeleteSelf   
  # 进程伪装的名称，暂未实现，bug较多
  -processName string
        ProcessName (default "kwoker")
  # 指定读取的profile文件
  -profile string
        Load Your Profile
  # cs服务端的.cobaltstrike.beacon_keys中读取出来的public key,需要base64编码
  -rsa string
        base64 rsa public key.
  # 保存的geacon文件名
  -s string
        Save name (default "Mgeacon")
  # CobaltStrike Host地址，就是监听器中的host地址,需加http://或者https://,有端口的加端口
  -u string
        CobaltStrike Host,Like:https://127.0.0.1:8443
```

## Supported Systems
| Arch  | Windows | Linux | MacOS |
|-------|---|---| --- |
| amd64 | ❌      | 🐕    | ❌ |
| 386   | ❌      | ❌    | ❌ |

根据项目热度后续更新更多系统和更多功能

## TODO
| 功能      | Windows | Linux | MacOS |
|---------|---|---| --- |
| 内存执行elf | ❌      | ❌    | ❌ |
| Job管理   | ❌      | ❌    | ❌ |
| 权限维持    | ❌      | ❌    | ❌ |

## 感谢以下项目

[geacon](https://github.com/darkr4y/geacon)

[geacon_pro](https://github.com/H4de5-7/geacon_pro)

[CrossC2](https://github.com/gloxec/CrossC2)
