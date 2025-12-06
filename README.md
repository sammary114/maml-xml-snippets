# maml-xml-snippets

本扩展提供用于 MAML（MIUI Application Markup Language for MORE）的 VS Code 代码片段，方便编写和维护基于 MAML 的界面描述 XML。

## 概述

MAML 最初用于 MIUI 的百变锁屏，以 XML + 特定语法描述锁屏界面。与 Android 的静态界面 XML 不同，MAML 支持时间线驱动的动态属性表达式——UI 会按帧率渲染并根据变量表达式实时更新，从而实现动画、交互和数据驱动的显示。MAML 引擎已从锁屏中独立，成为 MIUI 内置的通用界面描述与渲染框架，适用于时钟、天气小部件、闹钟界面等信息展示或轻交互场景。

本仓库包含一组实用的代码片段，帮助在 VS Code 中快速插入常用的 MAML 元素与属性，提升编写效率与正确性。

## 主要特性

- 常用 MAML 元素片段：快速插入 `Container`、`Text`、`Image`、`Animation` 等模板
- 动态属性与表达式示例片段，含时间/条件/变量绑定写法
- 示例与注释，便于新手理解 MAML 的渲染与帧率机制
- 轻量、零依赖，直接放入 VS Code 即可使用

## 安装

1. 将本仓库作为 VS Code 扩展或片段包安装，或直接在本地把 `snippets/` 目录放入用户片段目录。
2. 在 VS Code 中打开一个 MAML/ XML 文件（或 .xml），按 `Ctrl+Space` 调出补全，输入片段前缀（见下文）并回车插入。

## 快速上手

1. 打开或创建一个 MAML XML 文件。
2. 触发补全（`Ctrl+Space`）并输入片段前缀，例如 `maml-container`、`maml-text` 等。
3. 插入后根据注释替换占位符内容。

示例：插入一个基础容器与文本片段后，替换 text 与绑定表达式即可在运行时看到动态效果（取决于你的 MAML 引擎环境）。

## 仓库结构

- `snippets/` — 包含多个 VS Code 片段文件：
  - `capital.code-snippets` — 示例/大写前缀片段
  - `lower.code-snippets` — 示例/小写前缀片段
  - `snippet.code-snippets` — 常用 MAML 片段集合
- `README.md` — 本文件
- `package.json`、`CHANGELOG.md` 等扩展元信息

## 片段示例（说明）

- 前缀 `maml-container`：插入带有位置、大小与子元素占位的容器模板
- 前缀 `maml-text`：插入带样式与绑定表达式的文本节点模板
- 前缀 `maml-image`：图像元素模板，含缩放/资源引用示例

（具体的前缀与触发词请参考 `snippets/` 目录下的文件）

## 使用建议与注意事项

- MAML 是面向运行时渲染的标记语言，很多效果需要在目标设备或 MAML 引擎上预览才能完全呈现。
- 合理使用动态帧率与条件更新，避免无谓的全速渲染导致电量消耗。
- 本片段旨在提高编写效率，但不替代对 MAML 语法和引擎特性的深入理解。

## 贡献

欢迎提交 issue 或 PR：

- 修正或补充片段
- 添加更多示例与注释
- 增加针对特定场景的片段集合

在提交 PR 前请确保遵循仓库的代码风格与简洁注释要求。

## 许可

该项目使用 MIT 许可证（如果需要请根据实际情况替换为正确许可证）。

## 联系

如有问题或建议，请在仓库中打开 Issue，或联系维护者。

---

感谢使用 `maml-xml-snippets`，希望它能让你更快上手 MAML 开发。
