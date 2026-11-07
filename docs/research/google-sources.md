# Google 开发者文档风格指南：来源与覆盖说明

## 一、抓取与阅读方式

- **抓取日期**：2026-11-07（Asia/Shanghai）
- **抓取方式**：用 Python `urllib` 请求页面（自定义 User-Agent），以 `lxml` 提取 `<article>`/`<main>` 正文后阅读；全部目标页面返回 HTTP 200。
- **阅读范围**：逐页阅读 32 个页面（列表见下）；`/style/word-list` 共 532 个词条、约 11 万字符，采用「通读说明 + 按主题抽读词条」的方式，未逐条读完全部词条；`/style/code-syntax` 与 `/style/images` 为长页面，重点阅读了与规则集相关的章节（命令格式、占位符、alt 文本等）。
- **原文性质**：Google 明确说明该指南是 **guidelines, not rules**、是 Google 的 **house style**，不构成行业标准，也不打算取代其他风格指南；当偏离能让内容更好时可以偏离，但同一文档内要一致（见 https://developers.google.com/style/philosophy 与 https://developers.google.com/style）。
- **引用层级**（Google 的建议，供参考）：项目专用风格 > Google 本指南 > 第三方参考（拼写查 Merriam-Webster；非技术风格查 *The Chicago Manual of Style*；技术风格可参考 Microsoft Writing Style Guide）。

## 二、实际读过的页面（32 个）

| # | URL | 页面主题 | 在规则集中的主要用途 |
| --- | --- | --- | --- |
| 1 | https://developers.google.com/style | About this guide | 指南定位、引用层级、break the rules |
| 2 | https://developers.google.com/style/philosophy | Philosophy | house style 定位、非行业标准声明 |
| 3 | https://developers.google.com/style/highlights | Highlights | 核心要点总览（语气、语法、格式、图片） |
| 4 | https://developers.google.com/style/tone | Voice and tone | 语气、please、let's、感叹号、空话 |
| 5 | https://developers.google.com/style/sentence-structure | Sentence structure | 条件前置 |
| 6 | https://developers.google.com/style/procedures | Procedures | 程序步骤全部规则 |
| 7 | https://developers.google.com/style/lists | Lists | 列表类型、引导句、并行结构、标点 |
| 8 | https://developers.google.com/style/code-in-text | Code in text | 行内代码、代码字体对象、代码元素语法 |
| 9 | https://developers.google.com/style/code-samples | Code samples | 代码块、缩进、行宽、省略注释 |
| 10 | https://developers.google.com/style/ui-elements | UI elements and interaction | UI 元素命名、按钮图标、键盘键、介词、交互动词 |
| 11 | https://developers.google.com/style/accessibility | Write accessible documentation | 无障碍全部规则 |
| 12 | https://developers.google.com/style/translation | Write for a global audience | 全球化写作、简单词、helper words、术语一致 |
| 13 | https://developers.google.com/style/inclusive-documentation | Write inclusive documentation | 包容性语言、性别中性、ableist、非包容术语 |
| 14 | https://developers.google.com/style/jargon | Jargon | 行话处理 |
| 15 | https://developers.google.com/style/headings | Headings and titles | 标题句式、层级、格式 |
| 16 | https://developers.google.com/style/cross-references | Cross-references and linking | 链接文本、引导语、打开方式 |
| 17 | https://developers.google.com/style/word-list | Word list | 术语与用词（抽样，见下） |
| 18 | https://developers.google.com/style/commas | Commas | serial comma、逗号用法 |
| 19 | https://developers.google.com/style/dashes | Dashes | em dash、描述列表不用破折号 |
| 20 | https://developers.google.com/style/person | Second person and first person | you、祈使句、we 用法 |
| 21 | https://developers.google.com/style/voice | Active voice | 主动语态及例外 |
| 22 | https://developers.google.com/style/paragraph-structure | Paragraph structure | 段落规则 |
| 23 | https://developers.google.com/style/capitalization | Capitalization | sentence case、冒号大小写、冒号后大写例外 |
| 24 | https://developers.google.com/style/periods | Periods and end punctuation | 句号、引号/括号、感叹号、URL 句末 |
| 25 | https://developers.google.com/style/placeholders | Format placeholders | 占位符命名与解释 |
| 26 | https://developers.google.com/style/code-syntax | Document command-line syntax | 命令续行、可选/互斥/重复参数、click-to-copy |
| 27 | https://developers.google.com/style/notices | Notes, cautions, warnings | 提示框分级与使用限制 |
| 28 | https://developers.google.com/style/excessive-claims | Avoid excessive claims | 最高级、夸大声明 |
| 29 | https://developers.google.com/style/prescriptive-documentation | Prescriptive documentation | should vs must/can/might |
| 30 | https://developers.google.com/style/tense | Present tense | 现在时、将来时、would |
| 31 | https://developers.google.com/style/format-examples | Format examples | 举例的标点位置 |
| 32 | https://developers.google.com/style/images | Diagrams, figures, and other images | alt 文本、图片使用 |

### word-list 抽样说明

实际抽读并用于规则集的词条包括（按原页面词条名）：

`abort`、`above`、`access (verb)`、`allows you to`、`and/or`、`app`、`as`、`as of this writing`、`below`、`between versus among`、`can`、`check`、`choose`、`click`、`click here`、`currently`、`disable`、`drop-down`、`e.g.`、`earlier`、`easy, easily`、`email`、`enable`、`enter`、`etc.`、`execute`、`fill in; fill out`、`following`、`for example`、`functionality`、`future, in the future`、`hit`、`hover`、`i.e.`、`impact`、`just`、`later`、`leverage`、`login (noun or adjective), log in (verb)`、`master`、`slave`、`dummy variable`、`new, newer`、`once`、`page`、`please`、`press`、`runbook`、`select`、`setup (noun or adjective), set up (verb)`、`should, should be`、`sign into`、`simple, simply`、`since`、`tap`、`terminate`、`this, that`、`type`、`UI`、`user`、`using`、`utilize, utilization`、`we`、`while`、`you`、`sanity check`、`legacy`、`on-premises`、`filename`、`hostname`、`time zone (noun), time-zone (adjective)`、`documentation or document or documents`、`documentation set`、`button`、`dialog`、`tab`、`frontend`、`backend`、`Google, Googling`、`higher`、`lower`、`could`、`may`、`might`、`must`、`would`。

未逐一阅读的其余约 450 个词条：与本次「轻量写作 skill」的核心规则重合度低（大量为 Google 产品名、Android/Cloud 专属术语、单个技术名词拼写），且规则集有 80–120 条上限，故只抽取与通用软件文档写作最相关的词条。

## 三、未覆盖的页面及原因

以下页面**没有**作为独立页面读取（未在规则集中作为直接来源引用）：

| 页面 | 未覆盖原因 |
| --- | --- |
| /style/spelling | 未单独读；美式拼写规则来自 About 的引用层级与 Highlights 的概述，未核对拼写细节 |
| /style/abbreviations | 未单独读；缩写规则来自 /style/translation 与 /style/headings 的概述 |
| /style/pronouns、/style/articles、/style/prepositions、/style/contractions、/style/pluralization、/style/possessives、/style/anthropomorphism、/style/reference-verbs | 语言语法细分页，任务未要求；相关通用规则已由 person、voice、tense、translation 覆盖 |
| /style/colons、/style/ellipses、/style/hyphens、/style/parentheses、/style/quotation-marks、/style/semicolons、/style/slashes | 标点细分页，任务仅要求「commas、dashes 等标点页可选」；已读 commas、dashes、periods 三个核心页 |
| /style/dates-times、/style/numbers、/style/tables、/style/units-of-measure、/style/mathematical-notation、/style/phone-numbers | 格式细分页，未读；日期规则仅依据 Highlights/Translation 的概述，表格规则依据 Accessibility 页 |
| /style/text-formatting | 未读；格式一致性规则依据 Translation 页的概述 |
| /style/product-names、/style/trademarks、/style/filenames、/style/examples | 命名细分页，未读；本规则集只保留与通用写作最相关的复合词拼写规则 |
| /style/future、/style/timeless-documentation | 未单独读；时效词规则来自 word-list 的 `currently` / `as of this writing` / `future` 词条与 tense 页 |
| /style/other-sources | 未读；第三方内容指引未纳入（其原则与链接/引用规范有重叠，但未核对原文） |
| /style/api-reference-comments、/style/semantic-tagging、/style/html-formatting、/style/markdown | 未读；语义化规则依据 Accessibility 页的概述 |
| /style/headings-targets | 未读；标题作为链接目标的细节未纳入 |
| /style/whats-new | 未读；与规则蒸馏无关 |
| /style/code-syntax 第 261–500 行、/style/images 第 221–377 行 | 只读了与规则集相关的章节；命令输出格式、图片制作细节等未逐行阅读 |

## 四、Google house style 特有约定 vs 通用开发者文档原则

### 4.1 Google house style 特有约定（不要无条件套用）

这些条目是 Google 为其文档体系选定的约定，**不是行业标准**；目标项目可能有不同规范，采用前应确认：

1. **sentence case**：所有标题、文档题只用 sentence case（G-86、G-89）。
2. **American spelling / punctuation**：标准美式拼写（`color`、`canceled`）与美式标点（引号内句号、em dash 等）（G-93、G-96、G-118）。
3. **serial comma（Oxford comma）**：三项及以上并列时最后一项前加逗号（G-91）。
4. **em dash 用法**：只用 em dash、前后不加空格，不用 en dash（G-93）。
5. **"For more information, see ..."** 固定链接引导句式（G-103）。
6. **UI 元素名用粗体**、代码字体与粗体叠加的规则（G-57、G-58）。
7. **Google 特有的 UI 术语**：Google Cloud/Workspace 用 `field` 而非 `box`；控制台子页用 `page` 而非 `tab`；`dialog` 不写 `dialog box`（G-81）。
8. **`Optional:` 前缀**、子步骤用字母 + 罗马数字、菜单路径 `>` 的固定写法（G-32、G-33、G-34）。
9. **word list 的具体取舍**：`app` 优先于 `application`、`allows you to` → `lets you`、`click` 不写 `click on`、`e.g.`/`i.e.`/`etc.` 禁用、`master/slave` 替换等（G-66、G-67、G-69、G-70、G-78）。
10. **Google 产品名与组织自称**：如 `Google Cloud console`、`Google Workspace` 等固定名称；`we` 只指 Google/组织（G-03、G-81）。
11. **`please` 禁用**：Google 语气指南要求程序说明中不用 please（G-08）。
12. **版本范围用 `earlier` / `later`**（G-80）。
13. **文档自称 `this document`**、`documentation` 拼全称等具体用词（G-81）。

### 4.2 通用开发者文档原则（可跨组织采用）

这些条目与具体组织无关，属于开发者文档写作的通用最佳实践：

1. 用第二人称 `you` 称呼读者、指令用祈使句（G-01、G-02）。
2. 明确目标读者并保持一致（G-04）。
3. 优先主动语态、一般现在时（G-14、G-15）。
4. 条件/目的前置、关键信息前置（G-13、G-19）。
5. 短句、短段落、一段一个想法（G-17、G-18）。
6. 程序用编号步骤、一步一动作、步骤以祈使动词开头（G-27、G-28、G-29）。
7. 先写位置再写动作、动作在前结果在后（G-30、G-37）。
8. 不重复程序、只给一个最佳方法（G-40、G-41）。
9. 行内代码用 code font、代码示例正确格式化、占位符解释（G-45、G-46、G-49、G-50、G-55）。
10. 链接文本要描述性、不用 `click here`、不用 URL 作链接文本（G-102）。
11. 无障碍：语义化 HTML、键盘可达、alt 文本、不靠颜色单一线索、字幕/转录（G-104 至 G-111）。
12. 包容性语言：性别中性、避免 ableist 和比喻语言、替换非包容术语（G-78、G-114、G-115）。
13. 全球化写作：简单词、短句、避免习语/幽默/文化特定引用、术语一致、缩写首次定义（G-23、G-24、G-83、G-84、G-116、G-117）。
14. 避免主观评价词（simple/easy/quickly）和夸大声明（G-10、G-12、G-72）。
15. 避免方向性语言（above/below/right-hand side）（G-39）。
16. 术语和拼写一致、同一概念同一说法（G-84）。
17. 标题层级正确、不跳级、每页一个 h1（G-88）。
18. 列表类型与内容匹配、列表项并行（G-97、G-99）。
19. 提示框少用并分级（G-101）。
20. 行话能避免就避免，必须用时首次解释（G-85）。

### 4.3 判断说明

- 「通用原则」并不代表所有组织都必须照搬：例如「短句少于 26 词」来自 Google 的无障碍建议，是经验阈值，不是硬性语言规范。
- 部分条目介于两者之间：例如「避免 `should`」既是 Google 的 prescriptive documentation 约定，也与技术写作中「减少歧义」的通用目标一致；规则集在正文中按 Google 来源标注，采用时可结合项目语气调整。
- 本规则集所有「来源」均指向实际读过的页面；未读页面没有被伪装成来源。规则正文为中文转述与提炼，未整页复制原文。

## 五、规则数量与文件对应

- `research/google-rules.md`：119 条规则，7 组（语气与人称 12、句子与段落 14、程序步骤 18、代码与 UI 20、术语与用词 21、格式与标点 18、无障碍与全球化 16）。
- `research/google-sources.md`：本文件。
