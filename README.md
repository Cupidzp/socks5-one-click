# SOCKS5 一键部署与管理

基于 Gost 的 Linux SOCKS5 代理部署与管理入口。需要在 Linux 服务器上以 root 权限运行。

## 一键部署

```bash
curl -fsSL https://raw.githubusercontent.com/Cupidzp/socks5-one-click/main/S5 | sudo bash
```

脚本会下载并运行固定版本的部署管理脚本。初次配置时可设置端口和账号；默认密码为随机生成的 24 位字母数字串。部署后可在服务器终端运行 `S5` 打开管理面板。

## 脚本行为

- 安装 Gost，并配置 SOCKS5 服务及系统自启。
- 根据服务器环境配置防火墙放行规则。
- 提供重启、停止、日志、连通性测试和卸载选项。
- `S5` 快捷命令与面板更新均从本仓库获取启动入口。
