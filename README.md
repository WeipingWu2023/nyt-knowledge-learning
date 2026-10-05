# NYT Knowledge & English Learning

一个面向中文学习者的 Codex skill：把一篇可可靠读取的《纽约时报》（The New York Times，简称 NYT）文章，整理成适合 Obsidian 长期复习的双语学习笔记。

它把三件事放在同一份笔记里：

1. 先用非常简单的中文解释文章讲了什么、谁参与、事情如何发展，以及为什么重要。
2. 按文章原始顺序保留英文，逐句给出自然中文翻译，并挑选真正值得学习的词汇、固定搭配、语法和句子结构。
3. 把文章中的耐久知识连接到 Obsidian 的 `Knowledge` 知识笔记、其他文章笔记和英语学习笔记中，方便以后继续学习。

## 适合谁

- 想用真实新闻学英语的中文母语者。
- 需要先建立背景知识、又不想只看中文摘要的初学者。
- 使用 Obsidian 做长期知识管理的人。
- 想把一篇文章同时变成“英语课”和“知识卡片”的人。

## 核心原则

- 文章全文可可靠读取时才开始完整分析。
- 用户粘贴的文章正文是逐句翻译和语言分析的唯一主要依据。
- 不能可靠读取 NYT 全文时，不猜测、不拼接搜索摘要、不用第三方总结冒充原文。
- 遇到 CAPTCHA、付费墙、登录限制或自动化访问限制时，停止读取，并请用户粘贴全文。
- 文章来源和背景研究来源分开标注。
- 发布者已有的 Obsidian 笔记必须保留；创建概念笔记前先搜索现有 `Knowledge` 文件夹。
- 解释默认面向“会中文、电脑和 Obsidian 初学”的读者。

## 安装

### 方式 A：手动安装（最容易排查）

把本仓库中的 `nyt-knowledge-learning` 文件夹复制到你的 Codex skills 目录：

```text
Windows: %CODEX_HOME%\skills\nyt-knowledge-learning
macOS/Linux: $CODEX_HOME/skills/nyt-knowledge-learning
```

如果没有设置 `CODEX_HOME`，通常可以使用 Codex 配置目录下的 `skills` 文件夹。复制后重新打开或刷新 Codex，让它重新发现 skills。

安装后的结构应类似：

```text
nyt-knowledge-learning/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── access-and-input-modes.md
    ├── note-design.md
    └── research-and-sources.md
```

### 方式 B：Git 克隆

```bash
git clone https://github.com/<你的用户名>/nyt-knowledge-learning.git "%CODEX_HOME%/skills/nyt-knowledge-learning"
```

Windows PowerShell 示例：

```powershell
git clone https://github.com/<你的用户名>/nyt-knowledge-learning.git "$env:CODEX_HOME\skills\nyt-knowledge-learning"
```

把 `<你的用户名>` 换成仓库实际所属的 GitHub 用户名。

## 最简单的使用方法

安装完成后，直接在 Codex 中发送：

```text
请使用 nyt-knowledge-learning skill 分析这篇 NYT 文章：
<粘贴 NYT URL，或粘贴完整文章正文>
```

也可以直接说：

```text
请把下面这篇 NYT 文章整理成适合 Obsidian 的中英双语学习笔记。
```

如果系统没有自动识别 skill，可以明确写出：

```text
Use the nyt-knowledge-learning skill to turn this NYT article into a structured Obsidian learning note.
```

## 两种输入方式

### 1. 提供 NYT URL

```text
请分析这个 NYT 链接，并写入我的 Obsidian 知识库：
https://www.nytimes.com/...
```

Skill 会先尝试正常读取文章。如果正文完整可读，才会继续分析。

如果遇到付费墙、登录、验证码、机器人保护或其他限制，它应该停止，并准确告诉你：

> 我无法可靠读取这篇 NYT 的完整正文。请把文章正文复制给我。你不需要整理格式，直接全部粘贴即可。

这时把文章正文原样粘贴回来即可，不需要自己整理段落。

### 2. 直接粘贴文章正文（最可靠）

```text
请使用 nyt-knowledge-learning skill 分析下面的 NYT 文章。
我粘贴的内容是主要来源，请不要用搜索摘要补全缺失内容。

<文章标题、作者、日期和完整正文>
```

如果正文中混入了广告、导航栏或订阅提示，skill 可以忽略明显无关的界面文字，但不会擅自补写缺失段落。

## 输出内容

一份完整笔记通常包括：

1. 文章元数据：标题、作者、日期、主题和来源。
2. 初学者概览：用简单中文建立整体理解。
3. 背景知识：解释文章默认读者已经知道的概念。
4. 关键人物、组织、国家和概念。
5. 按原文顺序的段落和句子讲解。
6. 英语学习：高价值词汇、固定搭配、语法和句型。
7. 知识扩展、因果链和“为什么重要”。
8. 复习清单和 Obsidian 双向链接。
9. 分开的主要文章来源和背景研究来源。

简单句不会被机械地写成长篇语法课；复杂句和有迁移价值的表达会得到更多解释。

## Obsidian 文件约定

skill 默认使用以下 vault：

```text
D:\Obsidian\NYT
```

建议保持以下文件夹：

```text
Articles/          文章学习笔记
English learning/  可复用的英语表达和语法笔记
Knowledge/         跨文章复用的耐久知识
Templates/         Obsidian 模板
Dashboard/         学习总览
```

文章笔记使用可读文件名；耐久知识使用 `[[Knowledge/概念名]]`；相关文章使用 `[[Articles/文章名]]`。skill 会先搜索已有知识笔记，尽量更新和连接，而不是重复创建。

## 推荐提示词

### 只想先理解文章

```text
先不要逐句讲英语。请先用适合完全初学者的中文解释：发生了什么、谁参与、时间线是什么、为什么重要。然后再问我是否继续完整学习笔记。
```

### 想重点学英语

```text
重点讲解英文，不要逐个解释简单单词。请保留原句，给自然中文翻译，并解释高价值词汇、固定搭配、语法结构、语气和句子在段落中的作用。
```

### 想重点建立知识网络

```text
请重点检查 Knowledge 文件夹中已有概念，优先复用已有笔记；只为真正耐久、可跨文章复用的概念创建或更新知识笔记，并添加双向 wikilinks。
```

## 常见问题

### 为什么不能只给标题或搜索结果？

因为标题、摘要和第三方总结不能支持可靠的逐句翻译。缺少正文时，skill 必须明确说明，而不是猜测。

### 为什么有些事实会标记日期或“不确定”？

新闻事实可能变化，争议议题也可能存在不同解释。笔记会区分文章原文、背景研究和推断，并尽量保留时间和来源。

### 会不会删除我原来的 Obsidian 笔记？

不会。设计目标是保留原有内容；更新已有笔记时，也不应静默覆盖有冲突的内容。

### 是否需要先整理文章格式？

不需要。直接粘贴全文即可。只要文章正文基本完整，skill 会忽略明显的网页界面文字。

### NYT 文章有付费墙怎么办？

不要尝试绕过付费墙。请在你有权访问的情况下复制完整正文，再粘贴给 skill。

## 隐私与安全提醒

- 不要把你的 NYT 登录信息、密码、Cookie 或浏览器配置提交到仓库。
- 不要把包含私人文章、私人笔记、个人路径或 API key 的示例提交到 GitHub。
- 建议发布仓库时只包含本 skill 的说明、规则和引用文档，不要上传整个 Obsidian vault。

## 开源协议

本项目使用 MIT License。详见 [LICENSE](LICENSE)。
