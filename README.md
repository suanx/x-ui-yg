# xui-pox

x-ui 面板精简修改版一键安装脚本。

- 支持纯 IPv4、纯 IPv6,以及 AMD64 / ARM64 架构的 VPS 安装
- 支持 Alpine 系统,推荐使用最新版 Ubuntu
- 订阅节点本地化生成,不依赖第三方外链节点转换服务

## 一键安装

```
bash <(wget -qO- https://raw.githubusercontent.com/suanx/xui-pox/main/install.sh)
```

或

```
bash <(curl -Ls https://raw.githubusercontent.com/suanx/xui-pox/main/install.sh)
```

## 管理

安装完成后,在终端输入 `x-ui` 打开管理菜单。主菜单功能:

| 选项 | 功能 |
|---|---|
| 1 | 一键安装 xui-pox |
| 2 | 删除卸载 xui-pox |
| 3 | 其他设置(Argo 固定/临时隧道、本地 IP 订阅链接、hy2 多端口跳跃) |
| 4 | 变更面板设置(用户名密码、登录端口、根路径、还原面板) |
| 5 | 关闭、重启 xui-pox |
| 6 | 更新并查看聚合通用节点、clash-meta 与 sing-box 客户端配置及订阅链接 |
| 7 | 查看 xui-pox 运行日志 |
| 8 | 一键原版 BBR+FQ 加速 |
| 9 | 管理 Acme 申请域名证书 |
| 10 | 管理 Warp |
| 11 | 添加 WARP-plus-Socks5 代理模式(本地 Warp / 多地区 Psiphon-VPN) |
| 12 | 刷新 IP 配置及参数显示 |
| 0 | 退出脚本 |

## 仓库文件

| 文件 | 说明 |
|---|---|
| `install.sh` | 一键安装与管理脚本(主程序) |
| `config.json` | xray 默认出站配置模板 |
| `version` | 版本记录 |
| `ssh.yml` | 可选的服务器 SSH 保活工作流(需自行填写账户信息) |
| `xuiwpph_amd64` / `xuiwpph_arm64` | WARP-plus Socks5 二进制 |

## 说明

本版本已移除后台定时任务(自愈、开机自启、看门狗)、在线更新与版本检测功能,以及所有第三方推广内容。安装与升级请手动执行脚本。
