# 社区主题提交指南

核对日期：2026-09-29。仓库：<https://github.com/Tamako0401/Spectrum-Notes-Theme>。

## 当前状态

| 项目 | 状态 |
| --- | --- |
| 公开 GitHub 仓库 | Spectrum-Notes-Theme |
| 根目录 theme.css / manifest.json | 已准备，版本 0.1.0 |
| README 与展示截图 | 已准备；可使用 output/light-reading.png 或 output/dark-reading.png |
| 浅色 / 深色 | 已在本机 Obsidian 检查 |
| LICENSE | 尚未选择，提交前需补齐 |
| GitHub Release 及附件 | 尚未创建 |
| 社区目录账号关联与申请 | 尚未提交 |

## 当前提交流程

官方当前要求通过 [Obsidian Community](https://community.obsidian.md) 提交，不应直接沿用旧文章里的 community-css-theme.json PR 流程。

1. 补齐根目录 LICENSE，明确主题代码的使用许可。README 已有说明及相对路径截图；官方建议商店截图为 512 × 288，当前截图分辨率更大，可在正式提交前另做商店封面。
2. 核对 manifest：名称、作者、最低应用版本、版本号。目前最低版本写为 1.6.0，但仅在本机较新版验证；提交前应实际验证兼容性或提高最低版本。
3. 创建 GitHub Release。标签必须与 manifest 的 version 完全一致，例如 `0.1.0`，不要额外加 `v`；版本格式为 `x.y.z`。
4. 给该 Release 单独上传 `manifest.json` 与 `theme.css` 两个附件。仅有 GitHub 自动生成的源码 ZIP 或自行打包的主题 ZIP 不够。
5. 用 Obsidian 账号登录社区目录，在 Profile 中连接 GitHub。
6. 进入 Themes → New theme，填仓库 URL，选择 Owner，填截图的仓库相对路径，并勾选 Dark、Light。
7. 阅读并同意开发者政策及维护承诺后提交。目录读取默认分支 HEAD 的 manifest，因此默认分支与 Release 版本必须对应。
8. 根据自动审核反馈修复，增加版本并发布新 Release。可编辑介绍并选择 Publish，但审核错误未解决前不能在 Obsidian 内安装。

## 边上架边完善

不必等所有设想完成再提交。官方只要求首次提交；上架后，用户可在 Obsidian 内获取后续 GitHub Release。可以按 `0.1.0 → 0.1.1 → 0.2.0` 迭代，不要反复覆盖同一个版本的附件。

建议先处理已知兼容性问题并补 LICENSE、Release，再申请；移动端、Canvas、打印与插件兼容性继续逐项验证。没有实测的功能应在 README 如实注明。审核耗时没有在所查指南中给出保证。

## 代码要求和建议

- 开发者政策要求提供 LICENSE、遵守引用代码的原始许可，不得添加遥测或让主题从网络加载字体、图片等资源。
- 官方主题指南建议优先使用 CSS 变量，使用低优先级选择器，避免 `!important`，使用户能通过 CSS 片段覆盖。
- 当前主题没有远程字体/图片、网络调用或 `!important`。使用本地字体回退，无需安装第三方插件。这是静态检查结果，不代表社区审核已通过。
- 原主题源码不可得，本项目根据 PDF 视觉重新编写；不得将其描述为找回了原作者源码。

## 官方来源

- [Submit your theme](https://docs.obsidian.md/themes/app-themes/submit-theme)
- [Set up and claim](https://docs.obsidian.md/community-directory/set-up-and-claim)
- [Developer policies](https://docs.obsidian.md/community-directory/developer-policies)
- [Theme guidelines](https://github.com/obsidianmd/obsidian-developer-docs/blob/main/en/Themes/App%20themes/Theme%20guidelines.md)
