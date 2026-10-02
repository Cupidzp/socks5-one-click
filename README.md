# SOCKS5 一键部署与管理

基于 Gost 的 Linux SOCKS5 代理部署与管理入口，需要在 Linux 服务器上以 root 权限运行。

## 一键部署

```bash
curl -fsSL https://raw.githubusercontent.com/Cupidzp/socks5-one-click/main/S5 | sudo bash
```

仓库中的 `S5` 会下载固定版本的上游管理脚本，校验 Bash shebang 并运行 `bash -n` 后才执行。状态面板按监听端口判断用户是否运行，不依赖受限容器可能缺失的进程归属信息。

## 上游与版本

- 上游管理脚本：[Puthsent/S5 Gist](https://gist.github.com/Puthsent/36817edc52867fd74559fde96339af99)
- 集成修订：`adb37dc0fddee696944b38f921ae4c0f12736c77`（2026-10-01）
- Gost 核心：`go-gost/gost v3.3.0`；上游按内置 SHA-256 校验下载包。
- 初次配置会生成随机默认密码；管理面板提供多用户、独立端口及服务运维功能。

面板在线更新会回到本仓库启动器，因此保留语法检查和状态探测修复。
