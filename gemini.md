# 项目：AcademicLibrary (学术库) - Gemini 合作纲领 v4

## 1. 核心目标
- 建立一个结构化的个人学术知识库，用于深度阅读、理解和管理关键文献。
- 核心是为库中的每一篇精选论文，生成三个标准化的知识组件，并提供一个清晰的导航索引。

## 2. 每篇论文的核心产出 (The Three Key Artifacts)
- **`citation.bib` (文献引用)**: 纯粹的 BibTeX 格式引用条目，确保引用的准确性。
- **`summary.md` (论文精读)**: 对论文的深度解读和摘要，包括其核心思想、方法和结论。显然由gemini**中文**编写。
- **`advice.md` (引用建议)**: 关于如何在自己的论文中有效引用这篇文献的策略性建议。显然由gemini**中文**编写。

## 3. 最终目录结构
```
AcademicLibrary/
├── gemini.md           # 本文件，我们的合作纲领和长期记忆
├── downloads/          # 【下载暂存区】存放下载的、尚未处理或认为价值不大的论文。
└── library/              # 【核心知识库】存放所有精选论文及其产出。
    ├── README.md         # 【核心导航】所有已入库论文的索引和中文标题。
    └── 2408.12345/       # 用 arXiv ID 作为安全、唯一的文件夹名。
        ├── source/         # 【必须】存放原始文件 (特别是强调存储论文源码 .tex)。
        ├── citation.bib    # 【产出1】该论文的BibTeX引用。
        ├── summary.md      # 【产出2】对该论文的精读笔记。
        └── advice.md       # 【产出3】关于如何引用该论文的建议。
```

## 4. 最终工作流程
1.  **下载 (Download)**: 论文被下载到 `downloads/` 暂存区。
2.  **入库 (Ingest)**: 您筛选后，决定某篇论文值得精读，并指令我“入库”。
3.  **创建 (Create)**: 我将论文从 `downloads/` 移动到 `library/ID/source/`，并创建对应的文件夹结构。
4.  **生成 (Generate)**: 我分析论文，在 `library/ID/` 目录下生成 `citation.bib`, `summary.md`, `advice.md` 三个核心产出文件。
5.  **索引 (Index)**: 我自动更新 `library/README.md` 文件，添加新入库论文的条目，包含其中文标题和指向其文件夹的链接。
