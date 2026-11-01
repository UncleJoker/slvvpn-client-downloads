# SLVVPN 多端客户端下载安装

先安装目标设备的客户端，再从 SLVVPN 导出自己的 `.ovpn` 连接配置，最后导入并连接。

**123 云盘只提供下载说明；安装包请从下面的 GitHub 链接下载。** 无需为了获取安装包购买网盘会员。安装包和连接配置是两种文件，安装软件后仍需导入自己的配置。

| 目标设备 | 客户端与版本 | 安装入口 |
| --- | --- | --- |
| Windows 电脑 | OpenVPN Connect 3.9.0 | [下载 Windows 安装包（.msi）](https://github.com/UncleJoker/slvvpn-client-downloads/releases/download/clients-2026-10-11/openvpn-connect-3.9.0.5008_signed.msi) |
| Mac | OpenVPN Connect 3.8.2 | [下载 Mac 安装包（.dmg）](https://github.com/UncleJoker/slvvpn-client-downloads/releases/download/clients-2026-10-11/openvpn-connect-3.8.2.6009_signed.dmg) |
| 安卓手机／安卓平板 | OpenVPN for Android 0.7.65 | [下载安卓安装包（.apk）](https://github.com/UncleJoker/slvvpn-client-downloads/releases/download/clients-2026-10-11/ics-openvpn-0.7.65.apk) |
| iPhone／iPad | OpenVPN Connect | [前往 App Store 安装](https://apps.apple.com/app/openvpn-connect/id590379981) |

[完整下载列表](https://github.com/UncleJoker/slvvpn-client-downloads/releases/latest) · [English installation guide](INSTALL.en.md)

这里提供的是已核验的固定版本，不代表厂商最新版本。后续更新以本页链接为准。

## 1. 下载并安装

- **Windows**：在电脑浏览器打开上面的 Windows 下载链接，运行下载好的 `.msi`，按照安装向导完成安装。
- **Mac**：下载并打开 `.dmg`，按镜像内说明运行安装程序；若提供 Intel 和 Apple 芯片两个安装程序，请选择适合自己 Mac 的版本。根据系统提示授权安装与 VPN 配置。
- **安卓手机／安卓平板**：下载 `.apk`，按系统提示允许当前浏览器或文件管理器安装此应用，完成后打开 **OpenVPN for Android**。不要把它与 OpenVPN Connect 的界面混淆。
- **iPhone／iPad**：打开 App Store 安装 **OpenVPN Connect**。商店可用性取决于账号地区；MSI、DMG、APK 均不能在 iPhone／iPad 安装。

如果浏览器打开的是 Release 页面，请展开 **Assets**，选择 `.msi`、`.dmg` 或 `.apk`；`Source code (zip)`、`Source code (tar.gz)` 和 `complete-source.tar.gz` 是开发源码，不是安装包。

GitHub 或其安装包下载域名在部分网络下可能无法访问。遇到打不开时可稍后重试、换网络，或使用下面的厂商官方入口；无需购买 123 云盘会员解决此问题。

## 2. 导出并传输连接配置

1. 在 SLVVPN 的「设置 → 多端通用」选择自己的目标平台。
2. 点「导出证书」，按照页面提示生成 `.ovpn` 文件。能否导出以账号当前显示的资格为准。
3. 用系统分享、隔空投送或自己的文件传输工具，把 `.ovpn` 发送到目标设备。

`.ovpn` 含个人连接凭证，只传给自己的设备。不要上传到 GitHub、网盘公开分享或发送给他人。

## 3. 导入并连接

- **Windows／Mac（OpenVPN Connect）**：打开客户端，选择文件导入（Import Profile／File），选取 `.ovpn`，确认添加后启用连接。
- **安卓（OpenVPN for Android）**：打开客户端，选择导入，选取 `.ovpn` 并保存，再点保存的配置连接；允许系统添加 VPN 配置。
- **iPhone／iPad（OpenVPN Connect）**：把 `.ovpn` 保存到「文件」，再分享到 OpenVPN Connect 或在客户端选择文件导入，确认后连接并允许系统添加 VPN 配置。

已安装客户端的用户可以直接从第 2 步开始。证书过期或重新导出后，请导入新的 `.ovpn`；旧配置可能失效。

## 文件完整性、来源与许可证

Release 附有 `SHA256SUMS.txt`，可核对安装包完整性。安装包保持上游原始内容，未重新打包。本仓库是 SLVVPN 提供的下载入口，并非 OpenVPN 官方仓库。

- Windows／macOS：[OpenVPN Connect 官方入口](https://openvpn.net/client/)。版权属于 OpenVPN, Inc.；“OpenVPN” 是其注册商标。许可证和第三方组件通知见 Release 中的 `OpenVPN-Connect-EULA.pdf` 及安装包内通知。
- 安卓：[OpenVPN for Android 官方发布](https://github.com/schwabe/ics-openvpn/releases/tag/v0.7.65)，作者 Arne Schwabe；对应源码为 [v0.7.65](https://github.com/schwabe/ics-openvpn/tree/v0.7.65)。Release 同时提供 `Android-LICENSE.txt`、`GPL-2.0.txt` 和 `ics-openvpn-v0.7.65-complete-source.tar.gz`，后者包含该标签固定的子模块与构建文件。
- 官方安装文档：[Windows](https://openvpn.net/connect-docs/windows-installation-guide/)、[macOS](https://openvpn.net/connect-docs/macos-installation-guide/)、[iOS／iPadOS](https://openvpn.net/connect-docs/ios-installation-guide/)。

本仓库和 Release 不提供用户账号、SLVVPN 应用源码或个人 VPN 配置。
