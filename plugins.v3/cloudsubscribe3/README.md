# CloudSubscribe（网盘订阅助手）

MoviePilot V3 适配版网盘订阅助手插件。

- 支持 115、阿里云盘、天翼云盘、夸克等网盘的转存、跨盘转存、离线下载与洗版
- 多渠道（HDHive、PanSou 等）订阅缺失影视资源搜索
- STRM 生成、媒体库通知、自动榜单订阅、搜索渠道自动签到

## 安装

将本目录放置到 MoviePilot 的 `/config/plugins/cloudsubscribe`，或在插件市场中添加本插件仓库后安装。

## V3 适配

v3.0.0 起适配 MoviePilot V3：迁移至 `plugins.v3` 目录与 `app.sdk.*` 稳定 SDK，
数据库访问改用 `app.db.oper` 的 `Oper` 类，媒体身份统一为 `media_source + media_id`。

## 许可

GNU GPL v3.0，详见仓库根目录 [LICENSE](../../LICENSE)。
