# macos

通过github actions来运行macos

## 步骤

1. Fork下来这个项目
2. 在仓库设置里找到Secrets选项分别添加`FRPC_CONFIG_URL`,`SYS_USER`,`SYS_PASSWORD`
   > `FRPC_CONFIG_URL`填写你的frpc配置文件下载连接
   > `SYS_USER`填写你想使用的用户名(推荐使用root账户)
   > `SYS_PASSWORD`填写你想使用的密码
3. 点击仓库Actions, 选择workflow名字, 然后通过 `workflow_dispatch` 来启动

### 完成了！

> 账号和密码为你在变量设置的账号和密码，使用 `su - runner` 方可使用普通用户的身份进行

### 最后

之后通过ssh工具或者vnc工具连接
> 连接之后很奇怪？ 在会话中运行 `system_profiler SPHardwareDataType` 或使用 `pip3 install bpytop && bpytop`

### frpc 文件参考

```
[common]
server_addr = 远程外网ip
server_port = 7000

[ssh]
type = tcp
local_ip = 127.0.0.1
local_port = 22
remote_port = 23 #通过23端口连接mac ssh

[vnc]
type = tcp
local_ip = 127.0.0.1
local_port = 3283
remote_port = 3283

[vnc1]
type = tcp
local_ip = 127.0.0.1
local_port = 5900
remote_port = 5900
```
### 贡献者

- [rokibhasansagar](https://github.com/rokibhasansagar) - Author
- Team [Area69Lab](https://github.com/Area69Lab) for inspiring me into using macOS
- [P3TERX's ssh2actions](https://github.com/P3TERX/ssh2actions) for SSH-ing into Actions
- [xunri233](https://github.com/xunri233)

### 声明

```text
Please do not use this repository for 24x7x365 operations on GitHub.
请不要24小时不间断使用
Your account might get flagged or banned if GitHub Authorities want to do so.
这样做的话你的账户有可能会被标记或者封禁
Use this for education purposes only.
仅供参考学习

```
