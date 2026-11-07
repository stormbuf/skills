# Google 开发者文档风格参考

> 依据：Google Developer Documentation Style Guide，抓取日期 2026-11-07。本参考按主题整理为 119 条。
> 性质：guidelines, not rules——Google 的 house style，不是行业标准；偏离规则能让内容更好时可以偏离，但同一文档内保持一致。
> 优先级：项目专用规范 > Google 指南 > 第三方参考；拼写查 Merriam-Webster，技术风格可参考 Microsoft Writing Style Guide。
> 标记：`G-xx` 为本文编号，不是 Google 官方编号，便于对照；标「house style」的条目不要无条件套用到其他项目。

## 定位

- 目标：帮助开发者完成任务——准确、可扫描、可翻译、可访问；判断标准是读者能否快速找到并执行，形式统一让位于内容清楚。
- Google 指南是 house style，不是行业标准；偏离时保持同一文档内一致。
- 采用前先确认项目规范；项目规范与 Google 冲突时按项目规范。

来源：https://developers.google.com/style 、https://developers.google.com/style/philosophy

## 语气与人称

- 用 `you` / `your` 称呼读者，不用 `we` / `our` / `us` 指读者（G-01–G-03）；指令用祈使句，省略隐含的 `you`（G-02）。
- 开头明确读者是谁，全文保持一致（G-04）；语气像懂行又愿意帮忙的同行，自然、直接，不轻浮、不说教（G-05）。
- 不用俚语、网络缩写、流行文化梗、感叹号（G-06、G-07）。
- 程序说明不用 `please`、`please note`、`let's`（G-08、G-09）；删除 `simply`、`easy`、`quickly`、`at this time` 等空话和主观词（G-10、G-11）。
- 避免最高级与无法验证的夸大声明（G-12）。

来源：https://developers.google.com/style/person 、https://developers.google.com/style/tone 、https://developers.google.com/style/excessive-claims

## 句子与段落

- 条件、情境、目的放在指令前：`To delete the document, click Delete.`（G-13）；优先主动语态，让执行者作主语，被动只用于强调对象或执行者无关时（G-14）。
- 描述产品常态用一般现在时，不用 `will` / `would`（G-15、G-16）。
- 句子约 26 个词以内；一段一个中心思想，不超过 5–6 句（G-17、G-18）；关键信息放段首（G-19）；正文左对齐，不硬换行（G-20）。
- 避免双重否定；修饰语不超过两层，`only` 紧贴修饰对象（G-21、G-22）。
- 用简单词替代大词和短语动词：`start` 不用 `commence`，`use` 不用 `utilize`（G-23）。
- 补全 `then`、`that`、`of` 等 helper words，代词先行词必须明确（G-24–G-26）。

来源：https://developers.google.com/style/sentence-structure 、https://developers.google.com/style/voice 、https://developers.google.com/style/tense 、https://developers.google.com/style/paragraph-structure 、https://developers.google.com/style/translation

## 程序步骤

- 程序用编号步骤，不写成连续段落（G-27）；一步一个动作，步骤不能过长（G-28）。
- 每步第一句包含祈使动词，用完整句（G-29）。
- 先写工具、页面或字段，再写动作（G-30）。
- 有明确目标时用 `To...` 前置，如 `To start a new document, click File > New > Document.`（G-31）；可选步骤以 `Optional:` 开头（G-32）。
- 子步骤用小写字母，再下一层用小写罗马数字（G-33）；菜单路径用 `>`，小的连续点击可合并为一步（G-34）。
- 不把键盘快捷键写进步骤；必须按 Enter 时并入当前步（G-35、G-36）。
- 动作在前、结果在后，理由放在动作之后（G-37、G-38）。
- 不用 `above`、`below`、`right-hand side` 等方向语言（G-39）。
- 同一任务只给一个最佳方法；不重复已有程序，引用并链接（G-40、G-41）。
- 程序前用完整句引导，单步骤程序可写成句子或单个项目符号（G-42、G-43）；不写「run the following command」，说明命令完成什么（G-44）。

来源：https://developers.google.com/style/procedures 、https://developers.google.com/style/accessibility

## 代码与 UI

- 行内代码、命令、文件名、路径、参数用反引号（G-45）。
- 用代码字体的对象：属性名和值、类名、命令输出、数据类型、数据库元素、枚举值、环境变量、文件名/扩展名/路径、HTTP 状态码与动词、IAM 角色名、IP 地址、语言关键字、方法/函数名、包名、端口号、查询参数、占位符、用户输入文本（G-46）。
- 不用代码字体：域名、产品/服务/组织名、供读者在浏览器打开的 URL；URL 用描述性链接文本（G-47）。代码元素不变形、不作动词或名词：写 `Send a POST request`，不写 `POST the data`（G-48）。
- 代码示例按语言风格缩进，每行不超过 80 字符（G-49）；代码块用围栏，省略部分用对应语言的注释，不写 `...`（G-50）；示例前用完整句引导（G-51）。
- 命令续行：Linux / Cloud Shell 用 `\`，Windows 用 `^`，后续行缩进四格（G-52）；命令行语法 `[ARG]` 可选、`{A|B}` 互斥必选其一、`...` 可重复（G-53）；可一键复制的命令避免可选、互斥、重复参数（G-54）。
- 占位符用大写加下划线（如 `PROJECT_ID`），首次出现时解释；多个占位符用 `Replace the following:` 列表（G-55、G-56）。
- UI 元素名用粗体，不用引号（G-57）；标签大小写按页面，异常时统一 sentence case（G-58）。
- UI 元素名不作动词或名词；按钮按标签引用，图标按钮按 tooltip 引用（G-59、G-60）。
- 键盘键用 `Command`、`Control`、`Option`、`Shift` 拼写全称，组合键写 `MODIFIER+KEY`（G-61）。
- 交互动词精确：`click`（不用 `click on`）、`tap`、`press`、`select`（不用 `check`）、`enter`、`type`（G-62）。
- UI 介词：对话框、字段、列表、菜单、窗格、窗口用 `in`；页面、标签页、工具栏用 `on`（G-63）。
- 优先写任务目标，不堆 UI 细节：`Refresh the page.` 优于 `Click Refresh.`（G-64）。

来源：https://developers.google.com/style/code-in-text 、https://developers.google.com/style/code-samples 、https://developers.google.com/style/code-syntax 、https://developers.google.com/style/ui-elements 、https://developers.google.com/style/placeholders

## 术语与用词

- `user` 只指读者开发的软件的使用者，称呼读者用 `you`（G-65）；`app` 用于最终用户程序，`application` 用于复杂企业软件或固定短语（G-66）。
- `allows you to` 改为 `lets you` 或 `you can`（G-67）；`abort` / `terminate` 改 `stop` / `cancel` / `end`，`execute` 能改 `run` 就改（G-68）。
- 交互词：`select` 不用 `check`；`enter` 或 `type`；`click`；`hold the pointer over` 不用 `hover`（G-69）。
- 不用 `e.g.` / `i.e.` / `etc.`，改用 `for example` / `that is` / 明确的非穷尽引导语（G-70）；`leverage` / `utilize` 改为 `use`，`just` 通常是可删的填充词（G-71）；删除 `simple` / `easy` / `quickly` 等主观评价词（G-72）。
- 避免时效词：`currently`、`as of this writing`、`in the future`、`soon`；`new` 必须有参照点（G-73）。按语义选助动词：`must`、`can`、`might`、`We recommend`，不用含糊的 `should`（G-74）。
- 因果用 `because`，不用 `as` / `since` / `once`；`while` 表对比用 `although`；`this` / `that` 后补名词（G-75、G-76）。
- `between` 用于彼此区分的事物，`among` 用于群体；限定性从句用 `that`，非限定性用 `which` 加逗号（G-77）。
- 替换非包容术语：`allowlist` / `denylist`、`primary` / `replica`、`placeholder`、`quick check`（G-78）。
- 复合词拼写：`filename`、`hostname`、`frontend`、`backend`、`on-premises`、`email`、`time zone`（G-79，house style）；版本范围用 `or earlier` / `or later`，不用 `higher` / `lower`（G-80，house style）。
- 文档自称 `this document`；区分 `page`、`tab`、`dialog`；`UI` 不泛指页面（G-81）。`setup`（名词/形容词）/ `set up`（动词）；`login`（名词/形容词）/ `log in`（动词）；`sign in to`（G-82，house style）。
- 缩写首次出现写全称，低频缩写每次写全称（G-83）；同一概念全文用同一个词、同样拼写和大小写（G-84）；行话能避免就避免，必须保留时首次用括号简短解释或链接定义（G-85）。

来源：https://developers.google.com/style/word-list 、https://developers.google.com/style/inclusive-documentation 、https://developers.google.com/style/jargon 、https://developers.google.com/style/translation

## 格式与标点

- 标题和文档题用 sentence case（G-86，house style）；标题末尾不加句号（G-87）。
- 标题层级不跳级，每页只有一个 `h1`；任务型标题用动词原形，概念型标题用名词短语（G-88、G-89）；标题不用编号、不加链接、不留空标题（G-90）。
- 三项及以上并列用 serial comma（G-91，house style）；句首引导语后加逗号，两个独立分句由并列连词连接时连词前加逗号（G-92）。
- em dash 前后不加空格，不用 en dash 或连字符代替（G-93，house style）；冒号后首字母小写，专有名词、标题、引语、`Caution:` / `Note:` 标签除外（G-94，house style）。
- 句号后只留一个空格，URL 不放在句末（G-95）；引号、括号与句号的位置按美式惯例（G-96，house style）。
- 列表按内容选类型：有序用编号，无序用项目符号，术语解释用描述列表（G-97）；列表前用完整句引导，列表项保持并行结构与一致标点（G-98、G-99）；单项不用列表（单步骤程序除外），描述列表用冒号（G-100）。
- Note / Caution / Warning 少用并分级，不连续堆叠（G-101）。
- 链接文本要描述性，不用 `click here` 或 URL 作链接文本；独立引用用 `For more information, see ...`（G-102、G-103）。

来源：https://developers.google.com/style/capitalization 、https://developers.google.com/style/commas 、https://developers.google.com/style/dashes 、https://developers.google.com/style/periods 、https://developers.google.com/style/lists 、https://developers.google.com/style/notices 、https://developers.google.com/style/cross-references

## 无障碍与全球化

- 用语义化 HTML 和原生元素；标题用 `h1`–`h6`，强调用 `em`，代码用 `code`，键盘用 `kbd`（G-104）；键盘可达，并用屏幕阅读器测试（G-105）。
- 不靠颜色、大小、位置、形状等单一视觉线索传达信息（G-106）。
- 所有图片有 `alt`；装饰图用 `alt=""`；alt 简短（155 字符内），不写 `Image of`（G-107、G-108）。
- 新信息不放图片；不用图片展示文字、代码示例或终端输出（G-109）；音视频提供字幕或转录，不用闪烁元素（G-110）。
- 表格前用正文介绍，表头用 `th`，不合并单元格（G-111）；避免 camelCase 和全大写正文（G-112）。
- 不用标点承担关键语义；正文和标题不用 `&` 代替 `and`（G-113）。
- 用性别中性表达，避免 ableist 与比喻性语言（G-114、G-115）。
- 面向全球读者：简单词、短句、标准语序，避免习语、俚语、幽默、双关和文化特定引用（G-116）；示例中的人名、性别、年龄、地点要多样，避免地域特定引用（G-117）。
- 美式拼写是 house style，项目用英式或其他变体时按项目规范（G-118）；日期时间写清月份、时区或明确格式，避免 `03/04/2025` 这类歧义（G-119）。

来源：https://developers.google.com/style/accessibility 、https://developers.google.com/style/images 、https://developers.google.com/style/inclusive-documentation 、https://developers.google.com/style/translation

## 附：house style 与通用原则

- **不要无条件套用（house style）**：sentence case、美式拼写、serial comma、em dash、UI 元素粗体、`Optional:` 前缀、子步骤字母/罗马数字、`>` 菜单路径、Google 特定 UI 术语、版本 `earlier` / `later`。
- **可跨组织采用（通用原则）**：第二人称与祈使句、主动语态、短句短段、条件前置、编号步骤、代码字体、术语一致、无障碍、全球化写作、避免主观评价词。
- **落地方法**：先查项目规范；没有规定时按本文件；同一文档内保持一种选择，不混用。
