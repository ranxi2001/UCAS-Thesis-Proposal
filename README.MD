# 中国科学院大学研究生学位论文开题报告 LaTeX 模板

<div align="center">

**📖 基于2025年国科大开题报告官方Word模板精细优化 📖**

**最新维护 | 格式规范 | 开箱即用**

</div>

---

## 📋 项目简介

本项目提供了**中国科学院大学研究生学位论文开题报告**的 LaTeX 模板，严格遵循2025年国科大最新的开题报告格式要求。模板基于官方Word版本进行逐项对比和细节优化，力求在排版美观的同时完全符合学校规范。

相比其他版本，本模板具有以下特点：
- ✅ **最新规范**：依据2025年国科大开题报告Word模板细节打磨
- ✅ **完整章节**：包含所有必需的7个章节，符合最新报告提纲要求
- ✅ **字体优化**：封面标题使用AutoFakeBold技术实现宋体加粗，更接近Word效果
- ✅ **双面打印**：封面、摘要、目录后均有空页，适配双面打印需求
- ✅ **灵活配置**：支持第二导师、中英文摘要等可选项配置
- ✅ **开箱即用**：可直接上传Overleaf使用，无需复杂配置

## 📂 报告结构

本模板包含完整的开题报告章节：

1. **选题的背景及意义**
2. **国内外本学科领域的发展现状与趋势**
3. **课题主要研究内容、预期目标**
4. **拟采用的研究方法、技术路线、实验方案及其可行性分析**
5. **已有研究基础与所需的研究条件**
6. **研究工作计划与进度安排**
7. **参考文献**

## 🚀 快速开始

### 在线使用（推荐）

1. **下载项目**：点击右上角 `Code` → `Download ZIP`
2. **上传到 Overleaf**：打开 [Overleaf](https://www.overleaf.com/) 并上传 ZIP 文件
3. **设置编译器**：左上角 `Menu` → `Settings` → `Compiler` 选择 **XeLaTeX**
4. **开始编写**：修改 `Tex/Frontinfo.tex` 填写个人信息，在 `Tex/Mainmatter.tex` 撰写正文

### 本地编译

```bash
# 确保已安装完整的 TeX Live 或 MiKTeX
xelatex Thesis.tex
bibtex Thesis
xelatex Thesis.tex
xelatex Thesis.tex
```

或使用提供的脚本：
- **Windows**: 双击运行 `artratex.bat`
- **Linux/Mac**: 运行 `./artratex.sh`

## 📝 自定义配置

### 删除第二导师信息

如果不需要第二导师，可进行以下修改：

1. 删除 `Tex/Frontinfo.tex` 中：
```latex
\advisortwo{董超}% 第二指导老师
\advisortitletwo{研究员}% 第二指导老师职务
```

2. 删除 `Style/ucasproposal.cls` 中第 223 行：
```latex
\ucas@label@ch@advisor & \ulenhance{\ulextend[151pt]{\hspace*{-\ulhshift}\ucas@value@ch@advisortwo}}\ucas@label@ch@advisortitle\ulenhance{\ulextend[170pt]{\hspace*{-\ulhshift}\ucas@value@ch@advisortitletwo}}\\
```

### 删除中英文摘要

如果不需要摘要部分，删除 `Tex/Frontmatter.tex` 中相应的摘要代码块即可（详见文件注释）。

## 🔄 版本更新

### 2025 年更新
+ **2025.10.29** 修复封面标题字体为宋体1号加粗（使用AutoFakeBold实现更接近Word的效果）
+ **2025.10.29** 新增"研究工作计划与进度安排"章节，完善报告提纲结构

### 2023 年更新
+ **2023.10.14** 封面、摘要、目录后面都有一个空页，用于双面打印
+ **2023.10.14** 增加了中英文摘要 `Tex/Frontmatter.tex`
+ **2023.10.13** 奇数页页眉为章节标题，偶数页页眉为论文题目
+ **2023.10.13** 页码用阿拉伯数字编写，右页右对齐，左页左对齐
+ **2023.10.13** 分章节撰写时每章另起一页
+ **2023.10.13** 封面添加第二导师相关信息

## ⚠️ 已知问题

+ 目录格式与Word模板略有差异（LaTeX自动生成的格式更加规范）
+ 部分细节字体与Word可能存在微小差异（已尽力优化）

> 💡 **欢迎提交 Pull Request 或 Issue 来改进模板！**

## 📁 文件结构

```
UCAS-Thesis-Proposal/
├── Thesis.tex              # 主文档
├── artratex.bat/sh         # 编译脚本
├── Tex/
│   ├── Frontinfo.tex      # 封面个人信息
│   ├── Frontmatter.tex    # 摘要、目录等前置内容
│   └── Mainmatter.tex     # 正文内容
├── Style/
│   ├── ucasproposal.cls   # 文档类定义
│   ├── ucasproposal.cfg   # 配置文件
│   └── artratex.sty       # 样式包
├── Biblio/
│   └── ref.bib            # 参考文献数据库
└── Img/
    └── ucas_logo.pdf      # 国科大校徽
```

## 🤝 贡献与反馈

本项目基于 [ucasproposal](https://github.com/mohuangrui/ucasproposal) 模板开发，根据2025年国科大开题报告最新要求进行了全面优化和完善。

如果您在使用过程中发现问题或有改进建议，欢迎：
- 📮 提交 [Issue](https://github.com/your-repo/issues)
- 🔧 提交 Pull Request
- ⭐ 如果本项目对您有帮助，欢迎 Star 支持

## 📄 许可证

本项目继承原项目的开源许可，供学习交流使用。

## 🙏 致谢

感谢 [ucasproposal](https://github.com/mohuangrui/ucasproposal) 提供的基础模板，本项目在其基础上进行了针对性优化，力求完美适配2025年中国科学院大学开题报告的最新格式要求。

---

<div align="center">

**如果这个项目帮助到了您，请给个 ⭐ Star 吧！**

</div>
