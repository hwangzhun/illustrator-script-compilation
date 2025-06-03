# Illustrator 脚本集合

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

一个收集和汉化 Adobe Illustrator 脚本的仓库，包含原创脚本和对优秀开源脚本的本地化版本。

## 📦 内容概述

本仓库包含用于 Adobe Illustrator 的各种实用脚本，主要分为两类：

1. **原创脚本** - 由我自行开发的 Illustrator 脚本
2. **汉化脚本** - 对开源脚本的部分本地化版本

这些脚本旨在提高 Illustrator 的工作效率，自动化重复性任务，扩展软件功能。

## 📜 脚本列表

### 🛠️ 原创脚本
- [储存为PDF并转曲.jsx](/储存为PDF并转曲%20v0.4.jsx) - 一键导出转曲的PDF文件


### 🌐 汉化脚本

#### [对象与画板对齐 v0.2.jsx](/对象与画板对齐%20v0.2.jsx)
  
- 原脚本: AlignToArtboards.jsx
- 原作者：[creold](https://github.com/creold)  


该脚本会将选定的对象与其父画板对齐，或对齐文档中所有画板的内容。如果对象位于多个画板上，脚本会检查哪个画板包含该对象的中心，并与其对齐。如果对象的中心位于画板之外，则与第一个画板对齐。

> [!WARNING]   
> 选择的用于对齐的内容和对象的画板越多，脚本运行的速度就越慢。

![AlignToArtboards](https://i.ibb.co/XFQSmvR/Align-To-Artboards.gif)

---

#### [画板查找器 v0.2.jsx](/画板查找器%20v0.2.jsx)
  
- 原脚本: ArtboradsRemapper.jsx
- 原作者：[creold](https://github.com/creold)  

按名称或尺寸搜索画板，并在窗口中央显示选定的画板。宽度和高度以文档单位显示。按方向搜索时，横向、纵向和方形画板按尺寸降序显示。

![ArtboardsFinder](https://i.ibb.co/VJXKjWQ/artboards-finder.gif)

---

#### [画板名称重映射 v0.1.5.jsx](/画板名称重映射%20v0.1.5.jsx)
  
- 原脚本: ArtboradsRemapper.jsx
- 原作者：[creold](https://github.com/creold)  

将画板名称写入文本文件或从文本中应用。与“画板”面板中的数字对应的指定索引范围内。

![ArtboardsRemapper](https://i.ibb.co/xG8sSNr/Artboards-Remapper.gif)

---

#### [批量重命名器 v1.5.jsx](/批量重命名器%20v1.5.jsx)
  
- 原脚本: BatchRenamer.jsx
- 原作者：[creold](https://github.com/creold)  

批量重命名文档中的画板、顶层图层和选定对象。为名称添加通用前缀和后缀。“查找和替换”功能可替换当前名称中匹配的字符串。

**占位符** 

* {w} - 画板或所选对象的宽度（以文档单位为单位）
* {h} - 画板或所选对象的高度
* {u} - 文档单位（文档设置 > 单位）
* {nu:0} - 从输入的值开始自动升序编号
* {nd:0} - 从输入的值开始自动降序编号
* {c} - 文档颜色模型（RGB 或 CMYK）
* {d} - 当前日期 (YYYYMMDD)
* {fn} - 不带扩展名的文件名
* {n} - 要在“查找和替换”中替换的当前名称

查找和替换功能支持[正则表达式符号](https://cheatography.com/davechild/cheat-sheets/regular-expressions/)。例如：要删除姓名中的数字，请在“查找”中输入“\d”，并将“替换”保留为空白。要用其他字符替换空格，请在“查找”中输入“\s+”，并在“替换”中输入您要替换的符号。

> [!TIP]   
> 如果要更改行数，请将脚本文件中的 CFG `rows: 5` 更改为 `listHeight: 5 * 32` 中的相同值。`precision: 0` 设置画板和对象的高度和宽度的小数位数。

![BatchRenamer](https://i.ibb.co/p2VXbY9/Batch-Renamer.gif)

---

#### [平均颜色 v0.1.jsx](/平均颜色%20v0.1.jsx)
  
- 原脚本: AverageColors.jsx
- 原作者：[creold](https://github.com/creold)  

按名称或尺寸搜索画板，并在窗口中央显示选定的画板。宽度和高度以文档单位显示。按方向搜索时，横向、纵向和方形画板按尺寸降序显示。

![ArtboardsFinder](https://i.ibb.co/VJXKjWQ/artboards-finder.gif)

---

#### [画板名称重映射 v0.1.5jsx](/AlignToArtboards.jsx)
  
- 原脚本: ArtboradsRemapper.jsx
- 原作者：[creold](https://github.com/creold)  

将画板名称写入文本文件或从文本中应用。与“画板”面板中的数字对应的指定索引范围内。

![ArtboardsRemapper](https://i.ibb.co/xG8sSNr/Artboards-Remapper.gif)

对选定对象或组内或渐变内的对象进行颜色平均化。脚本会跳过无颜色或有图案的对象。如果未选择任何对象，脚本将处理文档中的所有组。它有两种模式：静默模式和对话框模式。可在 `CFG.showUI` 中更改。  

如果在运行脚本时按住 <kbd>Alt</kbd> 键，则无需编辑代码即可更改模式：

* <kbd>Alt</kbd> + `CFG.showUI: false` 对话框将显示
* <kbd>Alt</kbd> + `CFG.showUI: true` 静音模式，使用最新选项

![AverageColors](https://i.ibb.co/6bjPmLh/average-colors.gif) 

## ⚙️ 安装与使用

### 基本安装方法
1. 下载所需的 `.jsx` 文件
2. 在 Illustrator 中，通过菜单"文件 > 脚本 > 其他脚本"选择下载的脚本
3. 或者将脚本放入 Illustrator 的脚本文件夹实现快速访问:

   - **Windows**: 
     ```
     C:\Program Files\Adobe\Adobe Illustrator [版本]\Presets\zh_CN\脚本\
     ```
   - **Mac**: 
     ```
     /Applications/Adobe Illustrator [版本]/Presets/zh_CN/脚本/
     ```

### 使用提示
- 部分脚本可能需要特定版本的 Illustrator
- 首次使用建议备份当前文件
- 某些功能可能需要先选择对象再运行脚本

## ⚖️ 版权声明

### 原创脚本
所有原创脚本采用 [MIT 许可证](LICENSE)。

### 汉化脚本
汉化脚本遵循原作者的许可协议，每个脚本文件头部都包含原始版权信息。

特别感谢以下开发者的优秀工作：
- [creold](https://github.com/creold) 及其 [illustrator-scripts](https://github.com/creold/illustrator-scripts) 项目
- 其他脚本原作者

## 🤝 贡献与反馈

欢迎通过以下方式参与项目：

- 报告问题或建议：[新建 Issue](https://github.com/你的用户名/仓库名/issues)
- 提交改进代码：创建 Pull Request
- 分享你的原创脚本

### 汉化贡献指南
如需贡献新的汉化脚本，请确保：
1. 获得原作者的明确许可
2. 保留原始版权信息和许可协议
3. 在文件头部添加汉化者声明，例如：

```js
/**
 * 原脚本名: Original Script Name
 * 原作者: Author Name (https://github.com/author)
 * 原仓库: https://github.com/creold/illustrator-scripts
 * 汉化: Your Name (https://github.com/yourusername)
 * 汉化日期: YYYY-MM-DD
 * 原许可协议: MIT License
 */
