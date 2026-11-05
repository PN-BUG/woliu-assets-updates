# 发布维护

优先使用 source-0.1.1 附件中的 woliu-assets-publishing-tools-0.1.1.zip；维护工具提交 c41bed9ce56f4f7e953ab2ad4780fa19ff911ada，与安装包对应源码分别记录。

在开发仓库递增版本和 Android versionCode，运行专项回归与类型检查，提交后先生成对应源码，再依次构建 Windows/Web/Android/插件。使用 scripts/prepare-public-release.mjs 生成明确允许上传的文件。发布工具 scripts/publish-public-release.mjs 固定目标 PN-BUG/woliu-assets-updates，并核对 gh api user 身份。GitHub 凭据通过已登录 gh 或仅当前进程 GH_TOKEN 提供；严禁写入仓库。

固定版本先创建 draft/prerelease 并上传；服务端大小与 SHA-256 全部一致后发布。确认对应源码也已公开，然后更新 latest 说明和附件清单，最后将 pending-channels 提交到 main/channels。相同固定 tag 不覆盖；已有附件必须完全匹配。版本包、签名私钥、.env、联调收据、用户素材和账号数据不提交到本仓库。

匿名客户端下载和校验与认证上传分开执行。验证器不携带 GitHub token；需完整下载包并核对 SHA-256，不能把登录态上传成功当作公开下载成功。
