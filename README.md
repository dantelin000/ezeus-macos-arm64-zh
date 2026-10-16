# 宙斯＋波塞冬：Apple Silicon 程序与中文补丁

基于 eZeus 0.8.1-Beta.8 的 macOS ARM64 程序包，以及只适配此包的简体中文补丁。汉化已完成，并经实际游玩测试未发现明显问题。本项目负责分发整理、素材导入工具与汉化，不是原版游戏或 eZeus 官方发行。

**不含原版游戏素材。需要自行购买完整英文版《宙斯＋波塞冬》，并导入游戏素材及官方 eZeus 资源后运行。**

## 下载

请打开 [Releases 发布页](https://github.com/dantelin000/ezeus-macos-arm64-zh/releases/latest)，下载以下两个 ZIP；页面自动生成的 “Source code” ZIP 不是可安装程序。

| 文件 | 用途 | 大小 |
| --- | --- | --- |
| [eZeus-ARM64-macOS-no-assets.zip](https://github.com/dantelin000/ezeus-macos-arm64-zh/releases/download/v0.8.1-beta.8-zh.20261016/eZeus-ARM64-macOS-no-assets.zip) | ARM64 程序、原生素材导入器和依赖库 | 28.4 MB |
| [eZeus-ZH-CN-Patch-no-assets.zip](https://github.com/dantelin000/ezeus-macos-arm64-zh/releases/download/v0.8.1-beta.8-zh.20261016/eZeus-ZH-CN-Patch-no-assets.zip) | 专用中文差异补丁及安装工具 | 17.2 MB |

系统要求：**Apple Silicon Mac，macOS 15 或更高**。无需 Homebrew、Python、Rosetta 或重新编译游戏。使用已有 ARM64 引擎二进制；引擎本身仍为 Beta 版本。

## 安装

1. 购买并准备完整英文版 [GOG Zeus + Poseidon](https://www.gog.com/en/game/zeus_poseidon) 或 [Steam Zeus + Poseidon](https://store.steampowered.com/app/566050/Zeus__Poseidon/) 的已安装／合法解压游戏根目录。
2. 从 [官方 eZeus 0.8.1-beta 发布页](https://github.com/MaurycyLiebner/eZeus/releases/tag/0.8.1-beta) 下载并解压 `eZeus-0.8.1-beta.zip`，准备其中的引擎资源。
3. 解压程序包，把 `eZeus ARM.app` 拖入“应用程序”，启动后选择“导入素材”，依次选择上面两份资料的目录。
4. 退出游戏，运行补丁包中的 `eZeus 中文补丁.app`，选择“安装汉化”，然后重新启动游戏。

完整目录结构、导入要求、存档位置与恢复英文方法见 **[安装与导入 README](docs/安装与导入.md)**。两个 ZIP 内也附有此说明。

程序和补丁使用本机临时签名，未做 Apple 开发者签名或公证；首次打开可能需要按 macOS“隐私与安全性”的“仍要打开”流程操作。

## 内容与适配范围

- 中文差异文本涉及 7674 条游戏文字、1006 个消息字段及 10 份战役文本，另含内置界面翻译与自由字体。
- 补丁仅适配本仓库发布的 ARM64 0.8.1-Beta.8 程序包；不适用于零售 Windows 版或其他引擎版本。安装前校验引擎和英文文本指纹，支持恢复英文。
- 原版 DATA、音频、影片、地图、原始 ENG/XML、Windows 程序、个人存档，以及 `interface.e`、`i15.e`、`i30.e` 等贴图缓存均未随包分发。
- 程序写死的难度名称仍显示英文，部分教程图示以“图示略”标注，长中文含用于折行的空格。

## 校验与源码

[SHA256SUMS.txt](SHA256SUMS.txt) 对应本次发布的两个 ZIP。下载后可在同一目录运行：

```sh
shasum -a 256 -c SHA256SUMS.txt
```

两个应用的 `Contents/Resources/Source/` 内包含辅助工具源码及上游代码快照，`Contents/Resources/Licenses/` 内保留引擎、依赖和字体许可。来源、构建说明与适用许可见 [PROVENANCE.md](PROVENANCE.md)。

本仓库保存分发说明与校验值，可安装文件放在 Releases。原版游戏版权属于各自权利人，购买和素材导入由使用者自行完成。
