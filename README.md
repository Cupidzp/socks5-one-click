# SOCKS5 一键部署与管理

基于 Gost 的 Linux SOCKS5 代理部署与管理入口，需要在 Linux 服务器上以 root 权限运行。

## 一键部署

```bash
curl -fsSL https://raw.githubusercontent.com/Cupidzp/socks5-one-click/main/S5 | sudo bash
```

仓库中的 `S5` 会下载固定版本的上游管理脚本，先校验 Bash shebang 并运行 `bash -n`，通过后才执行。

## 上游与版本

- 上游管理脚本： [Puthsent/S5 Gist](https://gist.github.com/Puthsent/36817edc52867fd74559fde96339af99)
- 集成修订：`adb37dc0fddee696944b38f921ae4c0f12736c77`（2026-10-01）
- Gost 核心：`go-gost/gost v3.3.0`，下载包会按上游脚本内置的 SHA-256 值校验。
- 初次配置时会生成随机默认密码；管理面板提供多用户、独立端口及服务运维功能。

管理面板的在线更新会跟随上游 Gist 的最新版本。
