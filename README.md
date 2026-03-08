# 安卓封装说明

这个仓库现在已经整理成一个可直接用 Android Studio 打开的安卓壳工程，核心页面在 `app/src/main/assets/index.html`。

## 结构

- `app/src/main/assets/index.html`：你的魔方 HTML 页面，已调整为更适合手机触控，并改成完全离线运行。
- `app/src/main/assets/vendor/`：本地打包的 `three.js` 和 `OrbitControls`。
- `app/src/main/java/com/mofang/app/MainActivity.java`：安卓入口，使用 `WebView` 加载本地页面，并启用沉浸式全屏。
- `新建 文本文档.txt`：保留了你原始的 HTML 文本。

## 已完成

- 页面资源本地打包进 APP。
- 3D 引擎已经改成本地资源，完全离线可玩。
- 已补基础 APP 图标。
- 已补启动页。
- 已锁定横屏启动。
- 已补沉浸式全屏游戏模式。
- 已补 `Gradle Wrapper`，可直接执行 `gradlew` 构建。

## 构建 APK

### Android Studio

1. 用 Android Studio 打开当前目录。
2. 等 Gradle 同步完成。
3. 点击运行，或者直接执行 Build APK。

### 命令行

在项目根目录执行：

```bat
.\gradlew.bat assembleDebug
```

调试 APK 输出路径：

`app/build/outputs/apk/debug/app-debug.apk`

## 说明

- 项目已经在当前电脑上实际跑通 `assembleDebug`。
- 如果首次构建较慢，通常是因为 Gradle 和 Maven 依赖下载需要时间。
- `android-sdk/`、`tools/` 和本地缓存压缩包仅用于当前电脑构建，已加入忽略列表，不影响代码仓库提交。

## 如果你还想继续优化

- 我可以继续补发布签名配置。
- 我可以继续补 `release` 包名、版本号和混淆配置。
- 我也可以继续帮你生成 `AAB` 发布包。
