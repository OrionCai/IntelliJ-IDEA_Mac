# IDEA 使用

## IDEA 激活

1. 首先打开一次 IDEA
2. 从 https://3.jetbra.in/ 下载插件：`jetbra.zip`
3. 存放到想要的位置后，进入 scripts 目录打开终端，运行命令`sudo ./install.sh`
    1. 若报错:`Could not set environment: 150:Operation not permitted while System Integrity Protection is engaged` 
        1. 则需要关机进入恢复模式关闭 SIP（ M 系列芯片开机时长按解锁键，Intel 系列芯片长按 Command+R），选择“选项”，左上角终端输入`crsutil disable` ；
4. 运行后即可在网页复制激活码，激活即可
    1. 激活完毕后一定要恢复 SIP
        1. 关机进入恢复模式关闭 SIP（ M 系列芯片开机时长按解锁键，Intel 系列芯片长按 Command+R），选择“选项”，左上角终端输入`crsutil enable` ；
    2. 若激活后立马弹出激活界面（即激活失败）
        1. 左上角设置，更改 `language & region` 为 `America` ，再次激活即可

## IDEA 更新

- **如果使用MAC的多用户时，使用非默认（激活设备创建的用户）管理员用户登录时，idea 不会自动更新或下载任何驱动（除了插件）**
    - 例如：
        - `IDEA没有 /Applications/IntelliJ IDEA.app/Contents 的写入权限。请通过特权用户运行以更新。`
        - `Failed to download '[https://download.jetbrains.com/idea/jdbc-drivers/MySQL/8/LICENSE.txt'](https://download.jetbrains.com/idea/jdbc-drivers/MySQL/8/LICENSE.txt')：Remote host terminated the handshake`
- **解决方案：**
    - 进入 idea 应用目录的终端
    
    ```bash
    sudo chmod -R 755 .
    ```
