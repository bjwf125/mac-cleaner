# 拾净 · MacCleaner

用 Go 编写的 macOS 桌面清理工具。本仓库提供测试安装包与使用说明。

## 下载 0.9.0 测试版

- [下载 Universal DMG（推荐）](https://github.com/bjwf125/mac-cleaner/releases/download/v0.9.0-test.1/MacCleaner-0.9.0-macos-universal.dmg)
- [下载 ZIP 备用包](https://github.com/bjwf125/mac-cleaner/releases/download/v0.9.0-test.1/MacCleaner-0.9.0-macos-universal.zip)
- [发布说明与 SHA-256 校验文件](https://github.com/bjwf125/mac-cleaner/releases/tag/v0.9.0-test.1)

需要 macOS 12 或更新版本。Universal 包含 Apple Silicon 与 Intel 两个架构；窗口操作已在 Apple Silicon 上验证，Intel 尚未实机验证。

## 安装

打开 DMG，将 MacCleaner.app 拖到 Applications，然后从“应用程序”打开拾净。安装不会自动清理或启用定时任务。

当前为 ad-hoc 签名测试版，尚无 Developer ID 签名和 Apple 公证。通过网络下载后，macOS 可能阻止打开。请保留系统安全防护；正式发行将另行完成签名与公证。

## 本版功能

提供大文件清理、重复文件清理、相似照片清理、应用卸载、应用清理、开机启动项管理和磁盘空间分析。0.9.0 更新绿色卡片界面、扫描结果总览、筛选排序与按应用归组的缓存列表。

先扫描和预览，再选择处理；清理与卸载需确认，手动处理移到废纸篓，仍占用磁盘空间。运行中的应用、未确认归属的数据和受保护的应用沙盒目录会保留，沙盒目录会标明未扫描。

## 校验下载

将 DMG 与对应的 .dmg.sha256 下载到同一目录，在该目录运行：

```sh
shasum -a 256 -c MacCleaner-0.9.0-macos-universal.dmg.sha256
```

请下载 Assets 中的 MacCleaner 安装包。GitHub 自动生成的 Source code 压缩包仅包含这个下载仓库的文件，不是应用安装包。
