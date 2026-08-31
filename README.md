# MoviePilot-Plugins（CloudSubscribe V3 适配版）

网盘订阅助手（CloudSubscribe）MoviePilot V3 适配插件仓库。

本仓库由 [odomu/MoviePilot-Plugins](https://github.com/odomu/MoviePilot-Plugins) 的
`cloudsubscribe`（网盘订阅助手）插件迁移适配而来，目标是在 MoviePilot V3 上稳定运行。

## 功能简介

- 订阅搜索：多渠道（HDHive、PanSou 等）搜索缺失影视资源
- 网盘转存：支持 115、阿里云盘、天翼云盘、夸克等，支持跨盘转存与秒传
- 离线下载：ed2k / magnet / 磁力链接解析与离线任务管理
- STRM 生成、网盘洗版、媒体库通知
- 自动榜单订阅、搜索渠道自动签到（115 枫叶签到、夸克空间奖励签到）
- 支持媒体库联动与神医深度删除

## MoviePilot V3 适配说明（v3.0.0）

- 迁移至 `plugins.v3/cloudsubscribe` 目录，支持 V3 插件市场索引
- 全部导入切换至 `app.sdk.*` 稳定 SDK
- 数据库访问改用 `app.db.oper` 下的 `Oper` 类，弃用裸 `SessionFactory`
- 符号随 V3 变更：`NotificationType → MessageType`、`MessageChannel → NotificationChannel`、`Notification → Message`
- 订阅媒体身份统一为 `media_source + media_id`
- REST 响应统一 envelope 规范，移除 V3 已删除的 `MusicChain` 等模块

## 安装

MoviePilot V3 插件市场中添加本插件仓库后安装；或将 `plugins.v3/cloudsubscribe`
目录放置到 MoviePilot 的 `/config/plugins/cloudsubscribe`。

## 致谢

- 感谢原作者 **odomu** 开发并维护网盘订阅助手插件，本仓库为其在 MoviePilot V3 下的适配版本。
- 感谢 **MoviePilot** 项目及其插件开发文档、V3 插件适配指南提供的支持。
- 感谢 MoviePilot 插件社区及本插件依赖的开源项目（p115client、p123client、torf、curl_cffi、oss2、numpy、Pillow 等）。

## 许可

本项目基于 GNU GPL v3.0 许可发布，与原插件仓库许可一致。详见 [LICENSE](LICENSE)。
