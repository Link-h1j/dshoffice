# DshOffice

> 一个没有广告、没有会员弹窗、没有频繁升级打扰的日常办公入口。

DshOffice 是基于 [LibreOffice](https://www.libreoffice.org/) 26.8.2.2 源码重新编译、去品牌化的 Windows 办公套件，由 [Link-h1j](https://github.com/Link-h1j) 维护。

## 为什么做这个

WPS Office 和 Microsoft Office 功能确实强大，但用久了会发现：

- 打开先看广告 / 会员推广
- 隔三差五弹升级、登录、云服务提示
- 想要的功能藏在一层层会员权益后面

我只是想有一个“双击就能写文档、做表格、放 PPT”的入口。

所以我用 LibreOffice 的开源源码重新编译了一份：去掉捐赠按钮、去掉升级检查、去掉多余品牌，只保留最常用的办公能力。这就是 DshOffice。

## 下载与使用

1. 到 [Releases](https://github.com/Link-h1j/dshoffice/releases) 下载 `DshOffice-26.8.2.2-portable.zip`
2. 解压到任意目录（例如 `C:\DshOffice`）
3. 双击 `program\soffice.exe` 即可使用

绿色便携，不写系统目录，不需要安装。

## 包含什么

- Writer / Calc / Impress / Draw / Math / Base
- 支持 docx / xlsx / pptx 等常见格式
- 中文界面
- Skia 渲染
- 无广告、无捐赠按钮、无升级检查

## 与 LibreOffice 的关系

DshOffice 基于 The Document Foundation 的 LibreOffice 26.8.2.2 源码构建，遵循 MPL 2.0 许可证。

LibreOffice 是一款非常优秀的开源办公套件，**没有它就没有 DshOffice**。

DshOffice 是非官方构建，与 The Document Foundation 无隶属或背书关系。

## 我改了什么

- 产品名改为 DshOffice（窗口标题 / 关于 / 版本输出）
- 去掉捐赠按钮和捐赠横幅
- 去掉升级检查与更新推送
- 自定义蓝色 D 应用图标 + 按文件类型区分的文档图标
- Start Center 品牌图与「关于」里的 GitHub 按钮指向本项目
- 仅保留 en-US / zh-CN
- 禁用 Java / GPGME / Firebird / PDFium（换取更小、更稳定的构建）

## 已知限制

- 无自动更新：升级需要重新下载 Release
- 部分 Base 功能（Java 相关向导、GPGME 加密、Firebird 嵌入式库）不可用
- 安装目录内仍保留 MPL 2.0 协议头和 LICENSE/CREDITS 文件（开源协议要求，不能删除）

## 许可证

MPL 2.0，见 [LICENSE](LICENSE)。源码获取方式与修改清单见 [SOURCE.md](SOURCE.md)。

## 致谢

- [The Document Foundation](https://www.documentfoundation.org/) 与 LibreOffice 社区
- 所有让开源办公软件成为可能的人
