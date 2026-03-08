# MofangApp

`MofangApp` 是一个基于 `WebView` 的安卓魔方应用工程。项目核心页面位于 `app/src/main/assets/index.html`，页面资源与依赖已本地打包，可在离线环境运行。

## 项目结构

- `app/src/main/assets/index.html`：应用主页面，包含 3D 魔方界面、触控交互与自动还原逻辑。
- `app/src/main/assets/vendor/`：页面依赖资源目录，包含 `three.js`、`OrbitControls` 与魔方求解器相关脚本。
- `app/src/main/java/com/mofang/app/MainActivity.java`：安卓入口页面，负责加载本地资源并启用沉浸式全屏显示。
- `app/src/main/res/`：应用图标、启动页、颜色与主题等安卓资源文件。
- `新建 文本文档.txt`：原始 HTML 文本备份文件。

## 当前功能

- 本地资源加载，支持离线运行。
- 3D 魔方展示与触控交互。
- 随机打乱。
- 基于当前状态的自动还原。
- 横屏启动。
- 沉浸式全屏显示。
- Android Studio 与命令行构建支持。

## 构建方式

### Android Studio

1. 使用 Android Studio 打开项目根目录。
2. 等待 Gradle 同步完成。
3. 运行应用或执行 APK 构建。

### 命令行

在项目根目录执行：

```bat
.\gradlew.bat assembleDebug
```

调试 APK 输出路径：

`app/build/outputs/apk/debug/app-debug.apk`

## 构建说明

- 项目包含 `Gradle Wrapper`，可直接使用 `gradlew` 构建。
- 首次构建可能需要下载 Gradle 或 Android 相关依赖，耗时会相对更长。
- `android-sdk/`、`tools/` 与本地缓存压缩包用于当前环境构建，已加入忽略列表。

## 运行说明

- 应用面向 Android 设备。
- 页面资源已本地化，运行时不依赖外部 CDN。
- 自动还原功能基于当前魔方状态求解，不依赖操作记录回放。

## 后续可扩展项

- `release` 签名配置。
- `AAB` 发布包生成。
- 应用包名、版本号与发布配置整理。
