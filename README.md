# Woliu 素材库 · 下载与更新

基于 TagSpaces Lite 的本地优先素材管理软件，表情仓库为其中的图片子模块。本仓库提供公开测试包、更新清单、校验文件、发布说明和 AGPL 对应源码，独立于 Woliu 主站部署。

## 当前公开测试版 0.1.1

- Windows 10/11 x64：[安装包](https://github.com/PN-BUG/woliu-assets-updates/releases/download/windows-0.1.1/woliu-assets-win-x64-0.1.1.exe) · [便携 ZIP](https://github.com/PN-BUG/woliu-assets-updates/releases/download/windows-0.1.1/woliu-assets-win-x64-0.1.1.zip) · [版本说明](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/windows-0.1.1)
- Android 8+：[APK](https://github.com/PN-BUG/woliu-assets-updates/releases/download/android-0.1.1/woliu-assets-android-0.1.1.apk) · [版本说明](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/android-0.1.1)
- [网页静态包](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/web-0.1.1) · [Chrome/Edge 插件 0.2.1](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/extension-0.2.1)
- [对应源码与许可证](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/source-0.1.1) · [全部版本](https://github.com/PN-BUG/woliu-assets-updates/releases)

Windows 先选择本地文件夹再导入素材；导入复制来源文件。文件夹可设置压缩继承/开/关，原件保留。素材可加星级/标签/备注/保存筛选；表情分类不改变原文件。按需同步、文件夹权限、可撤销分享接入 Woliu 服务。

从工作台侧栏“下载与更新”或“关于 → 检查更新”查看当前平台版本和下载。旧 0.1.0 需先手动安装本版。安装由用户主动确认；Windows 便携版请先退出旧程序再解压到新目录，本地素材库原位置打开即可。Android 保留 com.woliu.memevault 包名与本机调试签名，覆盖安装需签名一致。插件解压后通过扩展管理的开发者模式加载。Web 包需 HTTP 静态托管。iOS 暂未提供安装包。

## 固定更新入口

| 平台 | 最新清单 | 固定发行页 |
| --- | --- | --- |
| windows | [JSON](https://raw.githubusercontent.com/PN-BUG/woliu-assets-updates/main/channels/windows.json) | [latest](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/windows-latest) |
| android | [JSON](https://raw.githubusercontent.com/PN-BUG/woliu-assets-updates/main/channels/android.json) | [latest](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/android-latest) |
| web | [JSON](https://raw.githubusercontent.com/PN-BUG/woliu-assets-updates/main/channels/web.json) | [latest](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/web-latest) |
| extension | [JSON](https://raw.githubusercontent.com/PN-BUG/woliu-assets-updates/main/channels/extension.json) | [latest](https://github.com/PN-BUG/woliu-assets-updates/releases/tag/extension-latest) |

清单记录平台、渠道、版本、架构、文件大小和 SHA-256，并指向固定版本附件。当前 channel=preview，GitHub 发布均为 prerelease；不作为稳定版本推广。历史固定版本保留，只有最新清单前移。应用仅接受本仓库 HTTPS 固定版本下载地址，不从其他项目获取更新。

## 测试边界

Windows 包未签名，Android 为调试包。依赖审计仍有 8 高危/4 中危告警，发布前需要处理；尚未完成 Android 真机及浏览器插件安装验收。Woliu 数据库迁移和本地服务连接真实数据库/Storage 的联调已通过，网站新入口仍未部署。普通密码登录验收需完成现有 CAPTCHA。

## 许可证与源码

这是独立维护的 Woliu 分支，与 TagSpaces 官方发行渠道分开。基于 [TagSpaces Lite v6.14.3](https://github.com/tagspaces/tagspaces/tree/v6.14.3)，AGPL-3.0；保留 TagSpaces GmbH 和第三方版权。完整对应源码、构建脚本、接口和许可证随 source-0.1.1 提供，构建源提交 fa9d592f5f6950a1f8948b648e52528ad878ec6f。安装包同时包含对应源码导出入口。本仓库 Git 历史只保存分发文档和更新清单。
