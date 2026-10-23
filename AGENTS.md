# Forge Android 开发约定

- 本目录是独立 Git 子模块 `forge-android`，包含 Kotlin 原生客户端 `nativeApp` 和兼容 WebView 客户端 `app`。只在本仓提交 Android 修改；主仓另行更新 gitlink。
- 子代理固定使用 `cn:deepseek-v4.1-flash`；失败不自动换模型。
- 运行时、Provider、密钥和会话存储属于 Core，Android 通过 HTTP RPC / WebSocket 连接，不复制 Core 实现。
- Gradle wrapper、版本和构建入口见 README。默认聚焦验证，不自动安装 APK、不重启设备或模拟器、不做正式发布。
- Node 联调 fixture 默认使用主仓内 `../repos/forge-core` 的构建产物；独立克隆时用 `FORGE_CORE_ROOT` 指定 Core 路径。
- 本地 SDK 配置、签名材料、模拟器日志、网络配置和构建产物不得提交。保留他人未提交改动；每轮自己的修改必须本地 commit，默认不 push。
