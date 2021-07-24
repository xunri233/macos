# macos

通过github actions来运行macos

## _步骤_

1. Fork下来这个项目
2. 在仓库的设置Secrets的分别添加`FRPC_CONFIG_URL`,`SYS_USER`,`SYS_PASSWORD`
   > `FRPC_CONFIG_URL`填写你的frpc配置文件下载连接
   > `SYS_USER`填写你想使用的用户名
   > `SYS_PASSWORD`填写你想使用的密码
3. 点击仓库Actions, 选择workflow名字, 然后通过 `workflow_dispatch` 来启动

### _完成了！_

> 账号和密码为你在变量设置的账号和密码，使用 `su - runner` 方可使用普通用户的身份进行

### _最后_

之后通过ssh工具或者vnc工具连接
连接之后很奇怪？ 在会话中运行 `system_profiler SPHardwareDataType` 或使用 `pip3 install bpytop && bpytop`


### _Credits_

- [rokibhasansagar](https://github.com/rokibhasansagar) - Author
- Team [Area69Lab](https://github.com/Area69Lab) for inspiring me into using macOS
- [P3TERX's ssh2actions](https://github.com/P3TERX/ssh2actions) for SSH-ing into Actions
- [xunri233](https://github.com/xunri233)

### _声明_

```text
Please do not use this repository for 24x7x365 operations on GitHub.
请不要24小时不间断使用
Your account might get flagged or banned if GitHub Authorities want to do so.
这样做的话你的账户有可能会被标记或者封禁
Use this for education purposes only.
仅供参考学习

```
