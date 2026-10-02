# SOCKS5 一键部署与管理

基于 Gost 的 Linux SOCKS5 代理部署与管理入口，需要在 Linux 服务器上以 root 权限运行。

## 一键部署

```bash
curl -fsSL https://raw.githubusercontent.com/Cupidzp/socks5-one-click/main/S5 | sudo bash
```

仓库中的 `S5` 会下载固定版本的上游管理脚本，校验 Bash shebang 并运行 `bash -n` 后才执行。启动器同时修正受限容器中 `ss` 不显示进程信息时的状态误报，并将面板更新导回本仓库启动器。

## 上游与版本

- 上游管理脚本：[Puthsent/S5 Gist](https://gist.github.com/Puthsent/36817edc52867fd74559fde96339af99)
- 集成修订：`adb37dc0fddee696944b38f921ae4c0f12736c77`（2026-10-01）
- Gost 核心：`go-gost/gost v3.3.0`；上游按内置 SHA-256 校验下载包。
- 初次配置会生成随机默认密码；管理面板提供多用户、独立端口及服务运维功能。
