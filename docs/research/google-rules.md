# Google 开发者文档风格指南规则蒸馏

本文件从 [Google Developer Documentation Style Guide](https://developers.google.com/style) 提炼，面向「轻量写作 skill」的参考规则集。抓取日期：2026-11-07。

**使用前提**

- 该指南自称 **guidelines, not rules**，是 Google 的 **house style**，不是行业标准。它明确说明：当偏离规则能让内容更好时，可以偏离，但在同一文档内要保持一致。
- 每条规则末尾的「来源」标注了属性：**通用原则** 表示跨组织普遍适用的开发者文档写法；**Google house style** 表示 Google 特有约定（如 sentence case、美式拼写、serial comma、特定 UI 术语），采用前应确认是否符合目标项目。
- 本规则集共 **119 条**，按 7 组组织。示例保持英文原样，便于直接对照原文。

---

## 一、语气与人称（12 条）

### G-01 用第二人称 "you" 称呼读者

- **规则**：直接称呼读者时用 `you` / `your`，不要用 `we` / `our` / `us` 指代读者。
- **为什么**：第二人称明确谁执行任务，语气直接、自然，避免读者误以为作者会替他们操作。
- **正例**：`The following sections describe how you can create a website.`
- **反例**：`The following sections describe how we can create a website.`
- **来源**：https://developers.google.com/style/person —— 通用原则

### G-02 指令用祈使句

- **规则**：要求读者做某事时用祈使句，隐含的 `you` 省略；在已经明确读者的行文中可以使用祈使句，但成组的操作应格式化为程序步骤。
- **为什么**：祈使句最短、最直接，减少歧义。
- **正例**：`Click Submit.`
- **反例**：`You should click the Submit button.`（在步骤语境中）
- **来源**：https://developers.google.com/style/person —— 通用原则

### G-03 第一人称复数只用于指组织

- **规则**：`we` / `our` / `us` 可以指文档署名的组织，但先行词必须清楚；不要用它们指读者。
- **为什么**：避免「谁来做」的歧义；组织自称与读者操作是两件事。
- **正例**：`For more information, contact our sales organization.`
- **反例**：`We can create the bucket by clicking Create.`
- **来源**：https://developers.google.com/style/person —— 通用原则

### G-04 明确并统一目标读者

- **规则**：在文档开头明确 `you` 是谁（开发者、系统管理员等），全文保持一致。
- **为什么**：不同读者的前置知识不同；读者群不清晰会导致解释过多或过少。
- **正例**：`This document is for data engineers who manage pipelines.`
- **反例**：全文时而面向开发者、时而面向最终用户，却不说明切换。
- **来源**：https://developers.google.com/style/person —— 通用原则

### G-05 对话、友好，但不轻浮

- **规则**：语气像「懂行又愿意帮忙的朋友」，自然、可接近；不要过度正式、说教或卖弄。
- **为什么**：开发者通常在赶任务，友好而直接的文字更易读；过度娱乐化会稀释信息。
- **正例**：`This API lets you collect data about what your users like.`
- **反例**：`Dude! This API is totally awesome!` / `The API documented by this page may enable the acquisition of information pertaining to user preferences.`
- **来源**：https://developers.google.com/style/tone —— 通用原则

### G-06 避免俚语、网络缩写和流行文化梗

- **规则**：不用 `tl;dr`、`ymmv` 等网络缩写，不用俚语、流行文化引用或刻意搞怪的措辞。
- **为什么**：这些表达对全球读者和翻译不友好，也容易过时。
- **正例**：`For a summary, see the overview.`
- **反例**：`tl;dr: see the overview.`
- **来源**：https://developers.google.com/style/tone —— 通用原则

### G-07 避免感叹号

- **规则**：概念、参考和程序文档中不用感叹号；只有代码语法、系统字面量或教程里程碑等少数场景可例外。
- **为什么**：感叹号显得不专业、可能引起警觉，而且翻译效果差。
- **正例**：`The VM is created.`
- **反例**：`The VM is created!`
- **来源**：https://developers.google.com/style/periods —— Google house style（但广泛适用）

### G-08 程序说明中不用 "please"

- **规则**：正常说明如何操作时不用 `please`，也不用 `please note`；只有请求许可或谅解时才用。
- **为什么**：步骤中的 please 属于过度礼貌，增加噪声，且翻译后可能显得奇怪。
- **正例**：`To view the document, click View.`
- **反例**：`To view the document, please click View.`
- **来源**：https://developers.google.com/style/tone —— Google house style（但广泛适用）

### G-09 避免 "let's"

- **规则**：不要用 `let's` 引导读者操作，改用祈使句或 `you can`。
- **为什么**：`let's` 把作者和读者混在一起，责任主体不明确。
- **正例**：`Consider adding a description to your table.`
- **反例**：`Let's add a description to our table.`
- **来源**：https://developers.google.com/style/tone —— 通用原则

### G-10 避免 "simply"、"easy"、"quickly" 等主观评价词

- **规则**：不用 `simple`、`simply`、`easy`、`easily`、`quick`、`quickly`、`careful`、`properly` 等词评价任务难度或要求读者态度。
- **为什么**：对专家简单的任务对新手可能很难；这类词带主观判断，还可能显得居高临下。无障碍与包容性写作也明确要求精确、客观。
- **正例**：`Open the configuration file and add your custom key.`
- **反例**：`Simply open the configuration file to quickly add your custom key.`
- **来源**：https://developers.google.com/style/inclusive-documentation —— 通用原则

### G-11 删除 "please note"、"at this time" 等空话

- **规则**：删除 `please note`、`at this time` 等不携带信息的铺垫语，直接陈述事实。
- **为什么**：这类短语增加篇幅、削弱重点，并让句子更难翻译。
- **正例**：`This feature isn't available.`
- **反例**：`Please note that at this time, this feature isn't available.`
- **来源**：https://developers.google.com/style/tone —— 通用原则

### G-12 避免夸大表述和最高级

- **规则**：不用 `best`、`fastest`、`simplest`、`never`、`always` 等最高级或绝对化表述；性能、成本、安全声明必须有可验证依据。
- **为什么**：无法验证的断言会损害文档可信度，也可能被未来事件推翻；竞品对比尤其容易失实。
- **正例**：`Using our security product is part of an overall strategy that helps prevent account takeovers.`
- **反例**：`Our security product prevents account takeovers.`
- **来源**：https://developers.google.com/style/excessive-claims —— 通用原则

---

## 二、句子与段落（14 条）

### G-13 条件、情境、目的放在指令前

- **规则**：如果要告诉读者在某种情况下做什么，先写条件/情境，再写指令。
- **为什么**：读者可以先判断条件是否适用，不适用时可跳过指令；也符合全局读者的阅读习惯。
- **正例**：`To delete the entire document, click Delete.`
- **反例**：`Click Delete if you want to delete the entire document.`
- **来源**：https://developers.google.com/style/sentence-structure —— 通用原则

### G-14 优先使用主动语态

- **规则**：让动作的执行者作句子主语，用主动语态；只有强调对象、弱化执行者或执行者无关时才用被动语态。
- **为什么**：被动语态容易隐藏「谁该做这件事」，让读者分不清是读者、服务器还是软件执行。
- **正例**：`The server sends an acknowledgment.`
- **反例**：`An acknowledgment is sent.`
- **来源**：https://developers.google.com/style/voice —— 通用原则

### G-15 描述一般行为用现在时

- **规则**：描述产品的一般行为、常态或事实时用一般现在时。
- **为什么**：现在时更直接、更「永恒」，避免 `will` 带来的时间歧义。
- **正例**：`Send a query to the service. The server sends an acknowledgment.`
- **反例**：`Send a query to the service. The server will send an acknowledgment.`
- **来源**：https://developers.google.com/style/tense —— 通用原则

### G-16 不用将来时或 "would" 描述产品常态

- **规则**：不要用 `will` 描述下一个版本才有的行为，也不要用假设性的 `would` 描述常规结果；真正发生在未来的动作可以用 `will`。
- **为什么**：文档应保持 timeless，预测未来会过时；`would` 让结果显得不确定。
- **正例**：`If you send an unsubscribe message, the server removes you from the mailing list.`
- **反例**：`You can send an unsubscribe message. The server would then remove you from the mailing list.`
- **来源**：https://developers.google.com/style/tense —— 通用原则

### G-17 句子尽量短

- **规则**：目标是把句子控制在 26 个词以内；能用短句说清就不要拉长。
- **为什么**：短句更易扫描、更易翻译；长句在翻译后会更长，可能造成排版和理解问题。
- **正例**：`Run the command. Then check the output.`
- **反例**：把多个条件、动作和结果塞进一个长句。
- **来源**：https://developers.google.com/style/accessibility —— Google house style（但广泛适用）

### G-18 一段只讲一个中心思想

- **规则**：每段聚焦一个想法；段落超过 5–6 句通常说明信息过载，应拆分或删减。
- **为什么**：读者是扫描式阅读，长段落会形成「文字墙」。
- **正例**：一段只解释一个概念，下一段再讲如何操作。
- **反例**：一段同时覆盖背景、步骤、限制和故障排查。
- **来源**：https://developers.google.com/style/paragraph-structure —— 通用原则

### G-19 段落关键信息前置

- **规则**：把段落最重要的信息放在第一句，不要把结论藏在段尾。
- **为什么**：读者不会逐字阅读，先看到重点才能决定是否继续。
- **正例**：`The API is unavailable in the EU. Requests from the EU return an error.`
- **反例**：先铺陈背景，最后一句才说 API 在 EU 不可用。
- **来源**：https://developers.google.com/style/paragraph-structure —— 通用原则

### G-20 段落左对齐、不强制断行

- **规则**：正文左对齐，不要居中、两端对齐或右对齐；不要在句子和段落中硬换行。
- **为什么**：硬换行在窗口缩放、不同设备或放大文字时会错位。
- **正例**：让文本自然回流。
- **反例**：在句子中间按 Enter 强制换行。
- **来源**：https://developers.google.com/style/paragraph-structure —— 通用原则

### G-21 避免双重否定

- **规则**：用肯定表达代替双重否定或层层例外。
- **为什么**：双重否定增加认知负担，也更容易误译。
- **正例**：`You can continue without a path.`
- **反例**：`A missing path won't prevent you from continuing.`
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-22 控制修饰语的数量和位置

- **规则**：不要用超过两个名词修饰另一个名词；`only` 等限定词要紧贴它修饰的词。
- **为什么**：名词堆叠和修饰语错位会造成歧义，翻译时尤其明显。
- **正例**：`A cloud-native DevSecOps pipeline in a hybrid environment` / `Request only one token.`
- **反例**：`A hybrid cloud-native DevSecOps pipeline` / `Only request one token.`
- **来源**：https://developers.google.com/style/translation —— 通用原则

### G-23 用简单词和单词代替大词、短语动词

- **规则**：用 `start` 代替 `commence`，用 `use` 代替 `utilize` / `leverage`，用 `some` / `many` 代替 `a number of`；尽量不用 `make use of` 这类短语动词。
- **为什么**：简单词更容易被全球读者理解，也更易翻译。
- **正例**：`This document uses the following terms:`
- **反例**：`This document makes use of the following terms:`
- **来源**：https://developers.google.com/style/translation —— 通用原则

### G-24 补全 then、that、of 等 helper words

- **规则**：在可能产生歧义的地方补出 `then`、`that`、`of` 等词，即使口语中常省略。
- **为什么**：这些词能明确条件和结果的先后关系、所属关系，降低翻译歧义。
- **正例**：`If the attribute key is not found, then the default value is returned.`
- **反例**：`If the attribute key is not found, the default value is returned.`
- **来源**：https://developers.google.com/style/translation —— 通用原则

### G-25 不省略关系代词

- **规则**：使用 `that`、`which` 等关系代词，不要省略。
- **为什么**：省略后句子结构不清晰，翻译器可能把从句和主句关系弄错。
- **正例**：`You can update the rules that you previously defined.`
- **反例**：`You can update the rules you previously defined.`
- **来源**：https://developers.google.com/style/translation —— 通用原则

### G-26 代词先行词必须明确

- **规则**：代词指代不清时，用名词替换代词。
- **为什么**：翻译常按句子或片段处理，脱离上下文的 `it` / `this` 无法正确翻译。
- **正例**：`If you use the term green beer in an ad, make sure that the ad is targeted.`
- **反例**：`If you use the term green beer in an ad, make sure that it's targeted.`
- **来源**：https://developers.google.com/style/translation —— 通用原则

---

## 三、程序步骤（18 条）

### G-27 程序写成编号步骤

- **规则**：程序（procedure）是一系列按顺序完成的动作，必须用编号列表；不要写成连续段落。
- **为什么**：编号让读者知道当前进度、不会漏步，也便于引用某一步。
- **正例**：`1. Click Create instance. 2. For Name, enter a name.`
- **反例**：把「先点哪里、再填什么」写成一段散文。
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-28 每步一个动作

- **规则**：一个步骤只包含一个动作；可以把小的连续动作合并，但步骤不能过长。
- **为什么**：一次一个决策，减少误操作；步骤太长读者容易迷失。
- **正例**：`Click Create instance.` 单独成步。
- **反例**：一步里同时创建实例、配置网络并部署应用。
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-29 步骤以祈使动词开头，用完整句

- **规则**：每个步骤的第一句必须包含祈使动词；用完整句子，不要用片段。
- **为什么**：读者能立刻知道要做什么；完整句更易翻译。
- **正例**：`Clone the repository that contains the sample data.`
- **反例**：`You need the project ID later in this document. Retrieve the project ID.`（前一句不是动作）
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-30 先写位置或环境，再写动作

- **规则**：说明读者在哪个工具、页面或字段里操作，再写具体动作；跨多个标题的程序要在每个程序首步重述环境。
- **为什么**：读者先定位再操作，减少来回查找；对屏幕阅读器和翻译也更友好。
- **正例**：`In Google Docs, click File > New > Document.`
- **反例**：`Click File > New > Document in Google Docs.`
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-31 步骤目标用 "To..." 前置

- **规则**：步骤有明确目标时，把目标写在动作前，如 `To start a new document, click File > New > Document.`；必要时用 `Start a new document: click ...` 澄清步骤是必需的。
- **为什么**：先说明目的，读者能判断这一步是否适用于自己，并理解动作的意义。
- **正例**：`To start a new document, click File > New > Document.`
- **反例**：`Click File > New > Document to start a new document.`
- **来源**：https://developers.google.com/style/procedures —— Google house style（但广泛适用）

### G-32 可选步骤用 "Optional:" 开头

- **规则**：可选步骤在步骤开头写 `Optional:`，不要写 `(Optional)`。
- **为什么**：统一前缀让读者一眼识别可跳过的步骤，也便于样式处理。
- **正例**：`Optional: Type an arbitrary string.`
- **反例**：`(Optional) Type an arbitrary string.`
- **来源**：https://developers.google.com/style/procedures —— Google house style

### G-33 子步骤用字母和罗马数字

- **规则**：编号程序的子步骤用小写字母（a、b、c），子子步骤用小写罗马数字（i、ii、iii）。
- **为什么**：与主步骤的数字区分层级，避免嵌套编号混乱。
- **正例**：`1. ...` → `a. ...` → `i. ...`
- **反例**：子步骤继续用 1、2、3，读者分不清层级。
- **来源**：https://developers.google.com/style/procedures —— Google house style

### G-34 菜单路径用 ">"，小动作可合并一步

- **规则**：连续菜单选择用 `>`（如 `File > New > Document`）；小的连续动作可以合并为一个步骤，用 `>` 表示顺序。
- **为什么**：路径写法紧凑、可扫描；避免把简单点击拆成过多步骤。
- **正例**：`Click Next > Finish.`
- **反例**：`Click Next. Then click Finish.`（作为两个独立步骤过细）
- **来源**：https://developers.google.com/style/procedures —— Google house style

### G-35 不把键盘快捷键写进步骤

- **规则**：不要在程序步骤中要求读者使用键盘快捷键；写界面操作，或提供可复制的命令。
- **为什么**：快捷键因操作系统和设置而异，且对部分读者不可用。
- **正例**：`Copy the command, and then paste it...`
- **反例**：`Press Ctrl+C, and then press Ctrl+V...`
- **来源**：https://developers.google.com/style/procedures —— Google house style

### G-36 需要按 Enter 时并入当前步骤

- **规则**：如果某一步之后必须按 Enter，把该说明写进同一步，不要单独列一步。
- **为什么**：按 Enter 是动作的一部分，拆开会让读者以为还有额外操作。
- **正例**：`Click the search box, type custom function, and then press Enter.`
- **反例**：`Click the search box and type custom function.` 然后另起一步 `Press Enter.`
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-37 动作在前，结果在后

- **规则**：步骤有结果时，先写动作，再在同一段写结果。
- **为什么**：读者先执行再观察反馈；顺序反过来会让人不知道先做什么。
- **正例**：`Click Run. The query results appear after the query runs.`
- **反例**：`The query results appear after the query runs. Click Run.`
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-38 理由放在动作之后

- **规则**：如果某一步需要解释理由，先说动作，再说原因。
- **为什么**：理由不阻塞执行；先给动作能让读者继续操作。
- **正例**：`Store the private key in a secure location. You need it later.`
- **反例**：`Because you need it later, store the private key in a secure location.`
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-39 不用方向性语言

- **规则**：不要用 `above`、`below`、`right-hand side` 等方向词定位文档内容或 UI；需要时提供截图或上下文。
- **为什么**：屏幕阅读器不呈现空间位置，RTL 语言的方向与 LTR 相反，翻译后位置描述也会失效。
- **正例**：`Click Menu.` / `In the preceding diagram, ...`
- **反例**：`In the left-side panel, click the button with three lines.` / `In the diagram above, ...`
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-40 同一任务只给一个最佳方法

- **规则**：一个任务有多种做法时，只记录一个对目标读者最合适的方法，优先选键盘可达、最短、最简单的做法；确有需要再分页、分标题或分标签展示。
- **为什么**：多个并列方法会增加选择负担，读者容易困惑。
- **正例**：只给出键盘可完成的最短步骤。
- **反例**：并列列出五种等价操作方式，却不说明何时用哪种。
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-41 不重复程序，引用已有步骤

- **规则**：重复出现的程序不要复制粘贴，改为引用并链接到已有程序。
- **为什么**：重复内容容易不同步，维护成本高。
- **正例**：`Create a user as you did in the previous step.`
- **反例**：把上一节的五步创建流程完整再抄一遍。
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-42 用完整句引导程序

- **规则**：程序前用完整句介绍，如 `To customize the buttons, follow these steps:` 或 `Customize the buttons:`；不要用被后续步骤补全的残句。
- **为什么**：完整句提供上下文，读者知道接下来要完成什么。
- **正例**：`To customize the buttons, follow these steps:`
- **反例**：`To customize the buttons:`
- **来源**：https://developers.google.com/style/procedures —— 通用原则

### G-43 单步骤程序可写成句子或单个项目符号

- **规则**：只有一个步骤的程序，可以写成普通句子，或用带引导句的单个项目符号。
- **为什么**：单个步骤用编号列表显得笨重；但单独一个项目符号可以强调操作。
- **正例**：`To clear (flush) the entire log, click Clear logcat.`
- **反例**：为一个点击操作硬造 `1.` 编号列表。
- **来源**：https://developers.google.com/style/procedures —— Google house style

### G-44 不写 "run the following command"，说明命令作用

- **规则**：不要用 `run the following command` 引出命令，改为说明这条命令完成什么，如 `Deploy the load generator:`。
- **为什么**：读者关心命令的目的，而不是「下面是命令」这个事实；说明作用更利于理解和检索。
- **正例**：`In Cloud Shell, deploy the load generator:`
- **反例**：`In Cloud Shell, run the following command:`
- **来源**：https://developers.google.com/style/procedures —— Google house style（但广泛适用）

---

## 四、代码与 UI（20 条）

### G-45 行内代码用 code font

- **规则**：正文中与代码相关的文本用 code font（HTML 用 `<code>`，Markdown 用反引号），表示按原样输入、界定边界并与周围文字区分。
- **为什么**：读者能一眼识别哪些内容要原样输入，减少复制错误。
- **正例**：`Set the CHROME_REMOTE_DESKTOP_DEFAULT_DESKTOP_SIZES environment variable.`
- **反例**：正文里直接写 `CHROME_REMOTE_DESKTOP_DEFAULT_DESKTOP_SIZES`，不加任何标记。
- **来源**：https://developers.google.com/style/code-in-text —— 通用原则

### G-46 这些代码对象要用代码字体

- **规则**：属性名和值、类名、命令输出、数据类型、数据库元素、枚举值、环境变量名、文件名/扩展名/路径、HTTP content-type、HTTP 状态码、HTTP 动词、IAM 角色名、IP 地址、语言关键字、方法/函数名、包名、端口号、查询参数、占位符、作为输入输出的字符串、用户输入文本等用代码字体。
- **为什么**：这些都是「代码实体」，统一标记能减少歧义。
- **正例**：`Call the get_job_status method.` / `Open the pg_hba.conf file.`
- **反例**：`Call the get job status method.`（把方法名拆成普通词）
- **来源**：https://developers.google.com/style/code-in-text —— 通用原则

### G-47 这些对象不要用代码字体

- **规则**：域名、产品/服务/组织名称、供读者在浏览器打开的 URL 不用代码字体；URL 通常应格式化为链接并使用描述性链接文本。
- **为什么**：它们不是要原样输入的代码；误用代码字体反而让读者以为要复制。
- **正例**：`You can find support at https://support.example.com.`（作为链接）
- **反例**：把 `example.com` 或产品名放进 code font。
- **来源**：https://developers.google.com/style/code-in-text —— Google house style（但广泛适用）

### G-48 代码元素不作英文动词或名词，不变形

- **规则**：不要把关键字、文件名等代码元素当动词或名词使用，也不要加复数或所有格；需要时在代码元素后加名词，再让名词变形。
- **为什么**：代码名不是自然语言词，随意变形会造成语法错误和翻译困难。
- **正例**：`The value of the ADDRESS constant is defined in the settings.h file.` / `Send a POST request.`
- **反例**：`ADDRESS's value is defined in settings.h.` / `POST the data.`
- **来源**：https://developers.google.com/style/code-in-text —— 通用原则

### G-49 代码示例的缩进与行宽

- **规则**：按对应语言的代码风格指南缩进（多数语言用空格、每级 2 空格）；每行不超过 80 字符，窄窗口或打印场景可更短。
- **为什么**：一致缩进和合理行宽让代码在网页、打印和代码审查中都易读。
- **正例**：两空格缩进、行宽 ≤ 80。
- **反例**：混用 Tab 和空格、单行超过 200 字符。
- **来源**：https://developers.google.com/style/code-samples —— Google house style（但广泛适用）

### G-50 代码块用 pre / 围栏，省略部分用注释

- **规则**：代码块标记为预格式化文本（HTML 用 `<pre>`，Markdown 用围栏）；省略代码时用该语言语法的注释说明，不要用三个点或省略号。
- **为什么**：正确的代码块保留空白和换行；用省略号会被误认为代码的一部分。
- **正例**：`# Several lines of code are omitted here.`
- **反例**：代码块中间写 `...`
- **来源**：https://developers.google.com/style/code-samples —— 通用原则

### G-51 代码示例前用完整句引导

- **规则**：代码示例前加一句介绍；介绍紧邻示例时用冒号，中间隔了说明段时用句号。
- **为什么**：读者先知道示例演示什么，才能正确理解代码。
- **正例**：`The following code sample shows how to use the get method:`
- **反例**：直接甩出一段代码，没有任何说明。
- **来源**：https://developers.google.com/style/code-samples —— 通用原则

### G-52 命令续行用 \ 或 ^，后续行缩进四格

- **规则**：命令一行超过 80 字符需要换行时，Linux/Cloud Shell 用 `\`、Windows 用 `^` 作为续行符；后续行缩进四个空格对齐。
- **为什么**：缺少续行符命令会执行失败；缩进让多行命令的结构一目了然。
- **正例**：`gcloud compute instances create INSTANCE_NAME \` 换行后缩进四格继续参数。
- **反例**：直接换行但不加 `\`，命令被 shell 拆成两条。
- **来源**：https://developers.google.com/style/code-syntax —— 通用原则

### G-53 命令行语法符号约定

- **规则**：`[ARG]` 表示可选参数，`{A|B}` 表示互斥必选其一，`...`（三个点、无空格）表示参数可重复。
- **为什么**：这些是命令行文档的通用记号，统一使用能准确表达参数约束。
- **正例**：`gcloud dns GROUP [GLOBAL_FLAG] [FILENAME]`
- **反例**：用 `<ARG>` 同时表示可选和必选，读者无法判断。
- **来源**：https://developers.google.com/style/code-syntax —— 通用原则

### G-54 click-to-copy 命令避免可选/互斥/重复参数

- **规则**：可一键复制的命令示例只保留完成最常见任务所需的参数；可选、互斥、重复参数用单独代码块展示，或链接到命令参考。
- **为什么**：方括号、花括号、竖线、省略号复制后会破坏命令。
- **正例**：`gcloud compute instances list`
- **反例**：`gcloud compute instances list [--zones=ZONE]`
- **来源**：https://developers.google.com/style/code-syntax —— Google house style（但广泛适用）

### G-55 占位符用大写加下划线，并解释一次

- **规则**：占位符用大写字母加下划线（如 `PROJECT_ID`），首次出现时解释其含义；不要用 `x` 或 `xxx` 作占位符（HTTP 状态码等标准场景除外）。
- **为什么**：描述性占位符让读者知道该替换成什么，减少猜测。
- **正例**：`Replace INSTANCE_NAME with the name of your new VM instance.`
- **反例**：`Replace X with the name.`
- **来源**：https://developers.google.com/style/placeholders —— Google house style

### G-56 多个占位符用 "Replace the following:" 列表

- **规则**：一个命令含两个以上占位符时，在命令后写 `Replace the following:`，按占位符在命令中出现的顺序逐项说明，每项以冒号加小写描述。
- **为什么**：读者可以逐项对照替换，不会遗漏或错配。
- **正例**：`Replace the following:` → `- ADMIN_PROJECT_ID: the project that owns the reservation`
- **反例**：把四个占位符的说明混在一段话里。
- **来源**：https://developers.google.com/style/placeholders —— Google house style

### G-57 UI 元素名用粗体

- **规则**：引用按钮、菜单、对话框、窗口、列表项等有可见名称的 UI 元素时，把名称加粗（HTML 用 `<b>`，Markdown 用 `**`）；不要用引号包住名称。
- **为什么**：粗体让 UI 名称在正文中突出，读者能快速定位；引号会让名称显得像普通引用。
- **正例**：`In the New project window, select the New activity checkbox, and then click Next.`
- **反例**：`In the New Project window, select "New Activity", and then click the "Next" button.`
- **来源**：https://developers.google.com/style/ui-elements —— Google house style

### G-58 UI 标签大小写按页面，异常时用 sentence case

- **规则**：一般遵循 UI 上的实际大小写；如果标签全大写或多个标签大小写不一致，统一用 sentence case。
- **为什么**：全大写难读，也不利于屏幕阅读器；统一大小写让文档更一致。
- **正例**：`Click Refresh.`（标签为 REFRESH）
- **反例**：`Click REFRESH.`
- **来源**：https://developers.google.com/style/ui-elements —— Google house style

### G-59 UI 元素不作动词或名词

- **规则**：不要把 UI 元素名称当动词或名词使用，应写清在哪个字段、菜单或按钮上操作。
- **为什么**：`Name the account` 之类的写法不清楚要点击或填写哪里。
- **正例**：`In the Name field, enter an account name.`
- **反例**：`Name the account.`
- **来源**：https://developers.google.com/style/ui-elements —— 通用原则

### G-60 按钮和图标按标签引用

- **规则**：按钮用其标签（如 `Click OK.`），不要写 `the "OK" button`；图标按钮用 tooltip 名称，并在名称前加图标；UI 名称末尾的省略号省略。
- **为什么**：标签是读者在界面上看到的文字，最可靠；描述图标外观（如「三条线按钮」）会因主题和语言而变化。
- **正例**：`Click Add.` / `Click Settings and utilities.`
- **反例**：`Click the icon.` / `Click Browse ....`
- **来源**：https://developers.google.com/style/ui-elements —— Google house style

### G-61 键盘键用 kbd，字母键大写、修饰键拼写全称

- **规则**：键盘键用 `<kbd>` 或等宽格式；字母键用大写；修饰键拼写为 `Command`、`Control`、`Option`、`Shift`；组合键写成 `MODIFIER+KEY`；多个系统并列时把 macOS 放在 Windows/Linux 后的括号中。
- **为什么**：符号（如 ⌘）在不同键盘和语言中不一致，拼写全称更通用。
- **正例**：`Press Control+C (or Command+C on macOS).`
- **反例**：`Press Ctrl+C (⌘+C).`
- **来源**：https://developers.google.com/style/ui-elements —— Google house style（但广泛适用）

### G-62 交互动词要精确

- **规则**：桌面鼠标环境用 `click`（不写 `click on`）；触摸设备用 `tap`；机械按键用 `press`；从多个选项中选择、选中文本或勾选复选框用 `select`（不用 `check`）；输入文本一般用 `enter`，强调键盘输入时用 `type`；泛泛选择可用 `choose`，UI 场景优先 `select`。
- **为什么**：不同设备与控件对应不同动作，精确用词能避免读者做错操作。
- **正例**：`Select the Automatically check for updates checkbox.` / `In the Owner box, enter your name.`
- **反例**：`Check Automatically check for updates.` / `Click on OK.`
- **来源**：https://developers.google.com/style/ui-elements、https://developers.google.com/style/word-list —— Google house style（但广泛适用）

### G-63 UI 介词要固定

- **规则**：对话框、字段、列表、菜单、窗格、窗口用 `in`；页面、标签页、工具栏用 `on`。
- **为什么**：统一介词让句子更自然，也减少翻译歧义。
- **正例**：`In the Alert dialog, click OK.` / `On the Edit tab, click Save.`
- **反例**：`On the Alert dialog, click OK.` / `In the Edit tab, click Save.`
- **来源**：https://developers.google.com/style/ui-elements —— Google house style

### G-64 优先按任务目标写，不堆 UI 细节

- **规则**：能用任务目标表达时，不要过度描述控件和手势，如 `Refresh the page.` 优于 `Click Refresh.`；只有在 UI 不明显或步骤目的就是引导界面操作时才细写。
- **为什么**：目标导向的写法更面向读者意图，也能在未来 UI 变化时保持有效。
- **正例**：`Expand the Advanced options section.`
- **反例**：`Click the arrow_right expander arrow next to Advanced options.`（除非确需说明控件）
- **来源**：https://developers.google.com/style/ui-elements —— 通用原则

---

## 五、术语与用词（21 条）

### G-65 "user" 只指读者开发的软件的用户

- **规则**：`user` 只用于指读者所开发软件的使用者；称呼文档读者一律用 `you`。
- **为什么**：混淆「读者」和「读者的用户」会让句子主体不清。
- **正例**：`This document shows you how to develop an app for your organization.`
- **反例**：`This document shows the user how to develop an app for their organization.`
- **来源**：https://developers.google.com/style/word-list —— 通用原则

### G-66 app 与 application

- **规则**：指面向最终用户的程序（尤其移动端或 Web）时用 `app`；企业软件等需要表达复杂度的场景可以用 `application`；`application programming interface` 等固定短语保留 `application`。
- **为什么**：`app` 更口语、更贴近开发者日常用法；固定短语不能随意替换。
- **正例**：`The app stores user preferences.`
- **反例**：`The application stores user preferences.`（普通移动应用语境）
- **来源**：https://developers.google.com/style/word-list —— Google house style

### G-67 不用 "allows you to"，用 "lets you"

- **规则**：`allows you to` 改为 `lets you` 或直接改写为 `you can`。
- **为什么**：更短、更自然，符合对话式语气。
- **正例**：`The API lets you collect data.`
- **反例**：`The API allows you to collect data.`
- **来源**：https://developers.google.com/style/word-list —— Google house style

### G-68 abort / execute / terminate 等词换用更简单的词

- **规则**：一般语境用 `stop`、`exit`、`cancel`、`end` 代替 `abort` / `terminate`；`execute` 能换成 `run` 时用 `run`；只有特定技术含义（如 Linux signal、网络终止）才保留原词。
- **为什么**：这些词常被泛化使用，语义模糊且语气生硬；简单词更清楚。
- **正例**：`Run the script.` / `Stop the process.`
- **反例**：`Execute the script.` / `Terminate the process.`（一般语境）
- **来源**：https://developers.google.com/style/word-list —— 通用原则

### G-69 交互动词与禁用词

- **规则**：勾选复选框用 `select`，不用 `check`；输入文字用 `enter`（一般）或 `type`（强调键盘输入）；点击用 `click`；不要用 `hit` 代替 click/press/type，不要用 `hover`，应写 `hold the pointer over`。
- **为什么**：这些词在 UI 语境中有明确对应动作，混用会让读者不确定该点击、按键还是悬停。
- **正例**：`Hold the pointer over File, and then click New.`
- **反例**：`Hover over File, and hit New.`
- **来源**：https://developers.google.com/style/word-list、https://developers.google.com/style/ui-elements —— 通用原则

### G-70 不用 e.g. / i.e. / etc.

- **规则**：`e.g.` 改为 `for example` 或 `such as`；`i.e.` 改为 `that is`；尽量避免 `etc.`、`and so on`、`and so forth`，改用能表达「非穷尽」的引导语。
- **为什么**：很多人混淆 e.g. 和 i.e.，拉丁缩写对全球读者也不友好；`etc.` 让列表边界含糊。
- **正例**：`Use a common image format, such as PNG or JPEG.`
- **反例**：`Use a common image format, e.g., PNG or JPEG, etc.`
- **来源**：https://developers.google.com/style/word-list —— Google house style（但广泛适用）

### G-71 leverage / utilize / just 等填充词

- **规则**：`leverage`、`utilize` 表示 `use` 时改用 `use`（`utilization` 指资源用量时可保留）；`just` 通常是可删除的填充词，需要时改用 `only`、`instead`、`previously`。
- **为什么**：大词并不更专业，反而增加阅读负担；删除填充词能让句子更直接。
- **正例**：`To distribute network traffic, use a load balancer.`
- **反例**：`To distribute network traffic, utilize a load balancer.`
- **来源**：https://developers.google.com/style/word-list —— 通用原则

### G-72 simple / easy / quickly 等主观评价词

- **规则**：删除 `simple`、`simply`、`easy`、`easily`、`quick`、`quickly` 等词，直接陈述操作或事实。
- **为什么**：任务难度因人而异，这类词带主观判断，可能让新手受挫。
- **正例**：`Open the configuration file and add your custom key.`
- **反例**：`Simply open the configuration file to quickly add your custom key.`
- **来源**：https://developers.google.com/style/word-list、https://developers.google.com/style/inclusive-documentation —— 通用原则

### G-73 避免带时效的表述

- **规则**：不用 `currently`、`as of this writing`、`in the future`、`soon`、`eventually` 等时效词；`new` / `newer` 必须给出参照点（版本号或日期）。
- **为什么**：文档应当 timeless，时效词会很快过期，也可能提前泄露产品计划。
- **正例**：`Windows isn't supported.`
- **反例**：`Windows isn't currently supported.` / `As of this writing, Windows isn't supported.`
- **来源**：https://developers.google.com/style/word-list —— 通用原则

### G-74 避免含糊的 should

- **规则**：按语义选择助动词：必须用 `must` 或祈使句；推荐用 `We recommend ...`；可选/能力用 `can`；可能用 `might` / `can`；不要用含义模糊的 `should`。
- **为什么**：`should` 介于「必须」和「可选」之间，读者无法判断是否必须执行。
- **正例**：`You must set the value to true.` / `You can also use approach B.`
- **反例**：`The value should be true.`
- **来源**：https://developers.google.com/style/prescriptive-documentation —— 通用原则

### G-75 因果用 because，不用 as / since / once

- **规则**：表示原因时用 `because`；`as`、`since` 可能指时间，`once` 可能指「之后」，都不要用来表因果。
- **为什么**：这些词多义，容易让读者误解时间关系。
- **正例**：`Because the cache is full, the request fails.`
- **反例**：`Since the cache is full, the request fails.`
- **来源**：https://developers.google.com/style/word-list —— 通用原则

### G-76 while 表对比用 although；this/that 后加名词

- **规则**：`while` 表示对比时改用 `although`；`this` / `that` 后尽量补一个名词，明确指代对象。
- **为什么**：`while` 也可指时间；裸 `this` / `that` 指代不清，翻译时尤其容易出错。
- **正例**：`Although the API is stable, the CLI is experimental.` / `This setting controls caching.`
- **反例**：`While the API is stable, the CLI is experimental.` / `This controls caching.`
- **来源**：https://developers.google.com/style/word-list —— 通用原则

### G-77 between / among、which / that 等易混词

- **规则**：`between` 用于两个或多个彼此区分的事物，`among` 用于群体中不区分的事物；非限定性从句用 `which` 并加逗号，限定性从句用 `that`。
- **为什么**：这些词混淆会改变句子的逻辑关系和范围。
- **正例**：`dependencies between the DOM, the CSSOM, and JavaScript execution` / `Name of the group, which has a maximum length of 200 characters.`
- **反例**：`dependencies among the DOM, the CSSOM, and JavaScript execution`（强调彼此关系时）
- **来源**：https://developers.google.com/style/word-list、https://developers.google.com/style/commas —— 通用原则

### G-78 替换非包容术语

- **规则**：不用 `master` / `slave`（改用 primary/replica、controller/worker 等）；`whitelist` / `blacklist` 改用 `allowlist` / `denylist`（必要时首次括注旧词）；`dummy` 改 `placeholder`；`sanity check` 改 `quick check` / `confidence check`。
- **为什么**：这些词带有歧视或暴力联想；如果代码里必须出现，只在代码字体中引用并尽量少用。
- **正例**：`Add the admin to the allowlist (sometimes called a whitelist).`
- **反例**：`Add the admin to the whitelist.`
- **来源**：https://developers.google.com/style/inclusive-documentation、https://developers.google.com/style/word-list —— 通用原则

### G-79 复合词拼写约定

- **规则**：`filename`、`hostname`、`frontend`、`backend` 各写一个词；`on-premises` 带连字符（任何词性）；`email` 不加连字符、不作动词；`time zone` 名词、`time-zone` 形容词。
- **为什么**：统一拼写避免同一概念出现多种形式，便于搜索和翻译。
- **正例**：`Open the filename field.` / `An on-premises database.`
- **反例**：`file name` / `on premise` / `e-mail`
- **来源**：https://developers.google.com/style/word-list —— Google house style

### G-80 版本范围用 earlier / later，不用 higher / lower

- **规则**：描述版本范围用 `or earlier` / `or later`；`higher` / `lower` 容易与版本号大小混淆。文档位置用 `earlier` / `preceding`、`later` / `following`。
- **为什么**：版本号不是数值大小，`higher` 可能让人误以为要比较数字；版本更新也可能回补旧版本。
- **正例**：`Use version 2.2 or later.`
- **反例**：`Use version 2.2 or higher.` / `Use version 2.2+`
- **来源**：https://developers.google.com/style/word-list —— Google house style

### G-81 document / page / tab / dialog / UI 的区分

- **规则**：指页面上的说明文字用 `this document`，不要用 `this article`、`this topic`、`this doc`、`this page`；`page` 指整个网页或控制台子页；控制台子页不要叫 `tab`；`dialog` 不要写 `dialog box`，`dialogue` 只指人与人对话；`UI` 不泛指页面，改用 `page`、`console` 或 `web interface`。
- **为什么**：这些词是文档导航的基本坐标，混用会让读者找不到位置。
- **正例**：`In the Google Cloud console, go to the Deployments page.` / `In the Welcome dialog, click OK.`
- **反例**：`In the Cloud Tasks UI` / `In the Deployments window`
- **来源**：https://developers.google.com/style/word-list、https://developers.google.com/style/ui-elements —— Google house style（但广泛适用）

### G-82 setup / set up、login / log in、sign in

- **规则**：名词或形容词用 `setup`，动词用 `set up`；名词/形容词用 `login`，动词用 `log in`；一般优先用 `sign in`，不写 `sign into`，应写 `sign in to`。
- **为什么**：词性不同拼写不同，混用会造成语法错误；`sign in` 比 `log in` 更通用。
- **正例**：`Run the setup script.` / `Set up the environment.` / `Sign in to the console.`
- **反例**：`Setup the environment.` / `Sign into the console.`
- **来源**：https://developers.google.com/style/word-list —— Google house style

### G-83 缩写首次出现要定义

- **规则**：缩写首次出现时写出全称，之后再用缩写；使用频率很低或只在局部出现的缩写，宁可每次都写全称。
- **为什么**：缩写脱离上下文难以理解，也不利于翻译。
- **正例**：`Google Kubernetes Engine (GKE)` 首次出现后使用 GKE。
- **反例**：标题里直接用 `GKE`，正文从未解释。
- **来源**：https://developers.google.com/style/translation、https://developers.google.com/style/headings —— 通用原则

### G-84 术语和格式保持一致

- **规则**：同一概念在全文中使用同一个词、同样的拼写和大小写；不要在不同段落用不同说法指同一事物。
- **为什么**：不一致会让翻译器误以为指不同概念，也会增加读者的理解成本。
- **正例**：全文统一使用 `allowlist`。
- **反例**：同一文档交替使用 `allowlist`、`whitelist`、`approved list`。
- **来源**：https://developers.google.com/style/translation —— 通用原则

### G-85 处理行话（jargon）

- **规则**：能用平实语言写清楚就不要用行话；必须保留行业术语时，首次出现用括号简短解释或链接到可信定义；不要为了 SEO 堆砌行话。
- **为什么**：行话只有特定群体理解，会阻碍全球读者和新手；但某些行业术语是读者搜索的关键词，可保留并解释。
- **正例**：`Move the task to an earlier part of the process (also known as shifting left).`
- **反例**：通篇使用 `shift left`、`blast radius` 而不解释。
- **来源**：https://developers.google.com/style/jargon —— 通用原则

---

## 六、格式与标点（18 条）

### G-86 标题和文档题用 sentence case

- **规则**：文档标题、章节标题只把第一个词、冒号后第一个词和专有名词首字母大写，其余小写。
- **为什么**：sentence case 更易读、更易扫描，也减少翻译时的大小写判断。
- **正例**：`Create a virtual machine`
- **反例**：`Create A Virtual Machine`
- **来源**：https://developers.google.com/style/capitalization —— Google house style

### G-87 标题末尾不加句号

- **规则**：标题和文档题不加句末句号。
- **为什么**：标题不是完整句子，句号会让它看起来像正文，也显得累赘。
- **正例**：`## Configure the network`
- **反例**：`## Configure the network.`
- **来源**：https://developers.google.com/style/periods —— Google house style（但广泛适用）

### G-88 标题层级不跳级，每页只有一个 h1

- **规则**：按 `h1 > h2 > h3` 的层级组织标题，不要从 `h1` 直接跳到 `h3`；每页只有一个一级标题；不要用标题标签改变视觉样式。
- **为什么**：正确的标题层级是屏幕阅读器和目录导航的基础；跳级会让结构混乱。
- **正例**：`h1` 下直接接 `h2`。
- **反例**：`h1` 后直接出现 `h3`。
- **来源**：https://developers.google.com/style/headings、https://developers.google.com/style/accessibility —— 通用原则

### G-89 任务型标题用动词原形，概念型标题用名词短语

- **规则**：任务型标题以 bare infinitive 开头（如 `Create an instance`）；概念型标题用名词短语（如 `Migration to Google Cloud`）；标题第一个词避免 `-ing` 形式。
- **为什么**：任务和概念在标题上可区分；`-ing` 开头在翻译时不一致，也增加字符数。
- **正例**：`Create an instance` / `Migration to Google Cloud`
- **反例**：`Creating an instance` / `Migrating to Google Cloud`
- **来源**：https://developers.google.com/style/headings —— Google house style（但广泛适用）

### G-90 标题里不用编号、链接和空标题

- **规则**：不要用数字给章节编号（靠层级和顺序表达）；标题中不加链接；不要出现没有内容的空标题。
- **为什么**：编号会和列表编号混淆；标题中的链接容易被误认为样式；空标题让目录出现无内容条目。
- **正例**：`## Estimate costs` 后紧跟正文。
- **反例**：`## 1. Estimate costs` / `## [Estimate costs](...)`
- **来源**：https://developers.google.com/style/headings —— Google house style（但广泛适用）

### G-91 三项及以上用 serial comma

- **规则**：三个或以上项目并列时，在最后的 `and` 或 `or` 前加逗号（Oxford comma）。
- **为什么**：避免最后两项被读成一组，改变原意。
- **正例**：`Locations are divided into zones, regions, and multi-regions.`
- **反例**：`Locations are divided into zones, regions and multi-regions.`
- **来源**：https://developers.google.com/style/commas —— Google house style

### G-92 逗号：引导语后、独立分句之间

- **规则**：句首引导词或短语后加逗号；两个独立分句由 `and`、`but`、`or` 等并列连词连接时，在连词前加逗号（两个分句都很短时除外）。
- **为什么**：帮助读者切分句子结构，避免把两个独立意思连读。
- **正例**：`Finally, only groups that contain parameters appear in this list.` / `The libraries make feed creation easier, and they ensure that only valid feeds are produced.`
- **反例**：`The libraries make feed creation easier and they ensure that only valid feeds are produced.`
- **来源**：https://developers.google.com/style/commas —— 通用原则

### G-93 使用 em dash，前后不加空格

- **规则**：表示句意中断或插入时用 em dash（—），前后不加空格；不要用 en dash 或连字符代替 em dash。
- **为什么**：em dash 是美式出版的标准用法；带空格的短横线在专业出版中不规范。
- **正例**：`This approach—while unusual—works.`
- **反例**：`This approach - while unusual - works.`
- **来源**：https://developers.google.com/style/dashes —— Google house style

### G-94 冒号后首字母小写（除非例外）

- **规则**：冒号后的第一个词通常小写；如果是专有名词、标题、引语，或 `Caution:`、`Note:` 等标签后的文字，则按相应规则大写。
- **为什么**：保持美式标点的一致惯例，避免随意的首字母大写。
- **正例**：`Open source software: Hadoop`（专有名词）
- **反例**：`The following items: Big, Small, and Medium.`（普通词不应大写）
- **来源**：https://developers.google.com/style/capitalization —— Google house style

### G-95 句子之间只留一个空格，URL 不放在句末

- **规则**：句号后只用一个空格；尽量不要把 URL 放在句子末尾，以免读者分不清句号是否属于 URL。
- **为什么**：两个空格在现代排版中不一致；URL 末尾的句号容易导致复制错误。
- **正例**：把 URL 单独放一行，行末不加句号。
- **反例**：`... at http://www.examplepetstore.com/privacy/.`
- **来源**：https://developers.google.com/style/periods —— Google house style（但广泛适用）

### G-96 引号、括号与句号的位置

- **规则**：句子以引号内容结尾时，句号放在引号内（即使句号不属于引文）；括号内是完整句子时句号放括号内，否则放括号外。
- **为什么**：这是美式英语的标点惯例，能保证句子边界清楚。
- **正例**：`... you might say "Fixed typo."` / `... (even if that change occurs while your application isn't running).`
- **反例**：`... you might say "Fixed typo".`
- **来源**：https://developers.google.com/style/periods —— Google house style

### G-97 按内容类型选择列表类型

- **规则**：有顺序的步骤、阶段、优先级用编号列表；无序的选项、示例用项目符号列表；术语加解释用描述列表（description list）。
- **为什么**：列表类型本身传达「是否有顺序」和「是否为术语解释」，选错会误导读者。
- **正例**：步骤用 `1. 2. 3.`，并列选项用 `-`。
- **反例**：把无顺序的功能列表写成编号列表，暗示有先后。
- **来源**：https://developers.google.com/style/lists —— 通用原则

### G-98 列表前用完整句引导

- **规则**：列表前用完整句提供上下文，句子以冒号或句号结尾；列表紧接引导句时用冒号，中间有说明段时用句号；标题已足够清楚时可以不写引导句。
- **为什么**：读者需要知道列表在回答什么问题，完整句比残句更清楚。
- **正例**：`Use the Submit button for any of the following purposes:`
- **反例**：`Use the Submit button to:`（残句，靠列表项补全）
- **来源**：https://developers.google.com/style/lists —— 通用原则

### G-99 列表项保持并行结构与标点一致

- **规则**：同一列表的项目使用相同的语法结构；每项首字母大写；完整句或含动词的项用句末标点，单词、无动词短语、纯代码或纯链接项不加句号。
- **为什么**：并行结构让列表易扫读；标点不一致会破坏节奏，也增加翻译难度。
- **正例**：`- Create an item. / - Replace one item with another. / - Update an item.`
- **反例**：`- Create an item / - Replacing items / - You should update.`
- **来源**：https://developers.google.com/style/lists —— 通用原则

### G-100 单项不用列表，描述列表用冒号

- **规则**：不要用列表只展示一个项目（单步骤程序除外）；描述列表用冒号或句号连接术语和描述，不要用破折号。
- **为什么**：单项列表浪费空间且显得结构异常；破折号会让术语和描述的关系不清晰。
- **正例**：`Example: This is an example.`
- **反例**：`Example - This is an example.`
- **来源**：https://developers.google.com/style/lists、https://developers.google.com/style/dashes —— 通用原则

### G-101 Note / Caution / Warning 少用并分级

- **规则**：提示框只在信息确实不属于正文流且重要时使用；Note 用于有用但非关键的信息，Caution 提醒谨慎，Warning 表示危险或不可逆操作；不要连续堆叠多个提示框。
- **为什么**：提示框过多会失去视觉显著性，读者会习惯性跳过。
- **正例**：用一段正文就能说清的补充信息不要做成 Note。
- **反例**：一页里连续放三个 Note，每个都只是补充说明。
- **来源**：https://developers.google.com/style/notices —— Google house style（但广泛适用）

### G-102 链接文本要描述性，不用 click here

- **规则**：链接文本用页面标题或能描述目标的短语，确保脱离上下文也能理解；不用 `click here`、`this document`、`read this`；不用 URL 作链接文本。
- **为什么**：屏幕阅读器用户常按链接跳读，链接文本必须自解释；`click here` 无法说明目标。
- **正例**：`For more information, see Load balancing and scaling.`
- **反例**：`Want more? Click here!`
- **来源**：https://developers.google.com/style/cross-references、https://developers.google.com/style/accessibility —— 通用原则

### G-103 链接引导语、重复链接与打开方式

- **规则**：独立句引用链接时统一用 `For more information, see ...` 或 `For more information about ..., see ...`；同一页面不要重复链接同一目标（长页面或不同入口除外）；默认在当前标签打开，若必须新标签打开要明确告知；下载文件或打开邮件也要在链接文本中说明。
- **为什么**：统一句式降低阅读成本；重复链接增加选择负担；意外的跳转行为会打断读者。
- **正例**：`For more information, see Load balancing and scaling.`
- **反例**：`For more information on indexes, see Manage indexes.`（用 on 而非 about）
- **来源**：https://developers.google.com/style/cross-references —— Google house style（但广泛适用）

---

## 七、无障碍与全球化（16 条）

### G-104 使用语义化 HTML 和原生元素

- **规则**：用语义标签表达结构（标题用 `h1`–`h6`，强调用 `em`，代码用 `code`，键盘用 `kbd`）；优先使用原生 HTML 元素，不要用自定义样式模拟按钮或表单控件。
- **为什么**：屏幕阅读器依赖语义结构；原生元素自带键盘和辅助技术支持。
- **正例**：`<button>` 做提交按钮，`<em>` 只表示强调。
- **反例**：用 `<div>` 加 CSS 模拟按钮。
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-105 键盘可达并做屏幕阅读器测试

- **规则**：确保读者只用键盘就能到达文档的所有部分（包括标签页、表单按钮和交互元素）；用屏幕阅读器测试文档。
- **为什么**：部分读者无法使用鼠标；屏幕阅读器测试能发现结构、链接和图片的隐藏问题。
- **正例**：用 Tab 键走完全部交互控件。
- **反例**：关键按钮只能鼠标点击。
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-106 不靠单一视觉线索传达信息

- **规则**：不要只用颜色、大小、位置或形状表达状态；如果使用颜色或图标表示状态，同时提供文字标签等第二线索。
- **为什么**：色盲、低视力或使用屏幕阅读器的读者可能接收不到纯视觉信息。
- **正例**：除了红色，还写 `Error: connection failed.`
- **反例**：只用红色圆点表示故障。
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-107 每张图片都要有 alt；装饰图用空 alt

- **规则**：所有图片必须有 `alt` 属性；有信息量的图写描述性 alt 文本，纯装饰图或与正文重复的图用 `alt=""`。
- **为什么**：屏幕阅读器、纯文本浏览器和低带宽用户依赖 alt；缺少 alt 时屏幕阅读器可能朗读文件名。
- **正例**：`alt="Architecture of an app built with Apps Script."`
- **反例**：`<img src="arch.png">`（没有 alt）
- **来源**：https://developers.google.com/style/images、https://developers.google.com/style/accessibility —— 通用原则

### G-108 alt 文本的写法

- **规则**：alt 文本用完整句或名词短语，简短（155 字符以内），不加 `Image of` / `Photo of`；考虑图片在上下文中的作用，而不是只描述画面内容。
- **为什么**：alt 是图片的替代文本，应传达意图；过长的 alt 会被屏幕阅读器打断。
- **正例**：`alt="A card message."`
- **反例**：`alt="Image of a card message that says hello."`
- **来源**：https://developers.google.com/style/images —— 通用原则

### G-109 新信息不要只放在图片里，不用文字/代码截图

- **规则**：不要在图片中引入正文没有的新信息；不要用图片展示文字、代码示例或终端输出，应该用真实文本；图表类图片要在正文提供等价说明。
- **为什么**：图片不翻译、不可搜索，屏幕阅读器也无法读取其中的文字。
- **正例**：代码用代码块展示，截图只用于必要的 UI 说明。
- **反例**：把一段终端输出截成 PNG 放在文档里。
- **来源**：https://developers.google.com/style/accessibility、https://developers.google.com/style/images —— 通用原则

### G-110 音视频提供字幕或转录，避免闪烁

- **规则**：音频、视频和 GIF 提供字幕、转录或文字描述；不要使用闪烁或闪光元素。
- **为什么**：听障读者需要文字替代；闪烁可能引发不适甚至癫痫。
- **正例**：视频附字幕和文字稿。
- **反例**：只有背景音乐和画面的教程视频，没有文字说明。
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-111 表格的无障碍写法

- **规则**：表格前用正文介绍；表头用 `th`；同时有行、列标题时用 `scope`；不要合并单元格（`colspan` / `rowspan`）；表格不是最佳呈现方式时改用列表。
- **为什么**：屏幕阅读器依赖表头和单元格关系朗读表格；合并单元格会破坏这种关系。
- **正例**：第一行和第一列使用 `th` 并标注 `scope`。
- **反例**：用合并单元格做复杂布局。
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-112 避免 camelCase 和全大写正文

- **规则**：正文中避免 camelCase 和全大写；必须使用代码标识符时放入代码字体。
- **为什么**：部分屏幕阅读器会把大写字母逐个读出，有些语言没有大小写概念。
- **正例**：`camel case` 这样的普通词用小写。
- **反例**：整段用 `THIS IS IMPORTANT` 强调。
- **来源**：https://developers.google.com/style/accessibility、https://developers.google.com/style/capitalization —— 通用原则

### G-113 不依赖标点传达含义，不用 & 代替 and

- **规则**：避免用感叹号、问号、分号等标点承担关键语义；除 UI 元素或代码中的 `&` 外，正文和标题不要用 `&` 代替 `and`。
- **为什么**：屏幕阅读器不一定朗读所有标点，部分读者会跳过标点；`&` 在朗读时可能被读成其他内容。
- **正例**：`You can continue.`（而不是用问号或感叹号表达语气）
- **反例**：`Name & address`（正文中）
- **来源**：https://developers.google.com/style/accessibility —— 通用原则

### G-114 使用性别中性的表达

- **规则**：避免默认男性或带性别刻板印象的词，如 `man-hours` 改 `person-hours`、`mankind` 改 `humanity`；示例中的性别和角色要多样。
- **为什么**：读者群体包含所有性别，性别化表达会排斥部分读者，也不准确。
- **正例**：`Equipment installation takes around 16 person-hours.`
- **反例**：`Equipment installation takes around 16 man-hours.`
- **来源**：https://developers.google.com/style/inclusive-documentation —— 通用原则

### G-115 避免 ableist 和比喻性语言

- **规则**：不用 `crazy`、`insane`、`blind to`、`cripple`、`dumb` 等残障歧视词；不用隐喻或比喻义，改用字面、精确的词。
- **为什么**：这类词会伤害残障读者，也容易误译；技术写作应使用字面语言。
- **正例**：`There are some baffling outliers in the data.` / `It slows down the service.`
- **反例**：`There are some crazy outliers in the data.` / `It cripples the service.`
- **来源**：https://developers.google.com/style/inclusive-documentation —— 通用原则

### G-116 面向全球读者：简单、短句、无习语和幽默

- **规则**：用简单词、短句和标准语序；避免习语、俚语、幽默、双关和文化特定引用。
- **为什么**：习语和幽默几乎无法直译，文化背景不同的读者也难以理解。
- **正例**：`Review what worked and what didn't.`
- **反例**：`Do a post-mortem and see what sticks.`
- **来源**：https://developers.google.com/style/translation、https://developers.google.com/style/inclusive-documentation —— 通用原则

### G-117 示例要多样，避免地域特定引用

- **规则**：示例中的人名、性别、年龄和地点要多样化；避免特定节日、文化习俗、体育项目或季节（如「八月是夏天」在南半球不成立）。
- **为什么**：示例会塑造读者对「典型用户」的想象，单一文化示例会排斥全球读者。
- **正例**：使用多个不同文化背景的虚构人名。
- **反例**：所有示例都叫 `John Smith`，并默认读者过圣诞节。
- **来源**：https://developers.google.com/style/inclusive-documentation、https://developers.google.com/style/translation —— 通用原则

### G-118 美式英语拼写（Google house style）

- **规则**：使用标准美式英语拼写和标点（如 `canceled`、`color`、`center`）；具体拼写以 Merriam-Webster 为首要参考。
- **为什么**：这是 Google 文档的 house style，能保证同一文档集内的拼写一致。**如果目标项目使用英式或其他变体，应按项目规范统一，不要盲目套用。**
- **正例**：`color` / `canceled`
- **反例**：`colour` / `cancelled`
- **来源**：https://developers.google.com/style、https://developers.google.com/style/highlights —— Google house style

### G-119 日期时间格式无歧义

- **规则**：日期和时间要写清楚月份、时区或采用明确格式，避免 `03/04/2025` 这类在不同地区含义不同的写法。
- **为什么**：全球读者的日期习惯不同，歧义会造成误解；文档中的时间点必须可复现。
- **正例**：`March 4, 2025, 14:00 UTC`
- **反例**：`03/04/25`
- **来源**：https://developers.google.com/style/translation、https://developers.google.com/style/highlights —— 通用原则

---

## 附：分组统计

| 分组 | 规则编号 | 条数 |
| --- | --- | --- |
| 语气与人称 | G-01 ~ G-12 | 12 |
| 句子与段落 | G-13 ~ G-26 | 14 |
| 程序步骤 | G-27 ~ G-44 | 18 |
| 代码与 UI | G-45 ~ G-64 | 20 |
| 术语与用词 | G-65 ~ G-85 | 21 |
| 格式与标点 | G-86 ~ G-103 | 18 |
| 无障碍与全球化 | G-104 ~ G-119 | 16 |
| **合计** |  | **119** |
