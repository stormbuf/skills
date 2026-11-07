# skills

> stormbuf 的 Skill 合集

每个技能都很小、可改、可组合，遵循通用 Skill 约定（`SKILL.md` + 参考文件），适配任何按该约定工作的 Agent。

## 安装

各 Agent 的技能目录不同，选对应方式；通用做法是把技能目录复制进去。

<details>
<summary><strong>dsh / 其他遵循 <code>~/.agents/skills</code> 约定的 Agent</strong></summary>

```bash
git clone https://github.com/stormbuf/skills.git
cp -R skills/skills/writing/stormbuf-tech-writing-style ~/.agents/skills/
```

本仓库是技能内容的存放处；实际安装在 `~/.agents/skills/`（多数 Agent——含 ZCode——默认加载该目录），更新时从仓库复制覆盖。

</details>

<details>
<summary><strong>skills.sh 安装器</strong></summary>

```bash
npx skills add stormbuf/skills -g -y -s stormbuf-tech-writing-style -a <agent>
```

`-a` 指定安装目标 agent。省略 `-a` 时安装器会写入它检测到的所有 agent。

</details>

## 技能参考

按调用方式分：**User-invoked** 只能由你点名触发；**Model-invoked** 可由你点名，也会被 Agent 按任务自动选用。

每个技能的自我介绍（是什么、为什么存在、适用场景、来源授权）都写在技能目录下的 `README.md`，根 README 只维护索引——这是对所有技能的常态要求。

### writing

**Model-invoked**

- **[stormbuf-tech-writing-style](skills/writing/stormbuf-tech-writing-style/README.md)**: 技术写作风格控制——`google`、`ste`、`hybrid`（默认）三种模式，按内容块切换。详细介绍、适用场景与来源授权见其目录下的 README。

## 仓库结构

```text
skills/<类别>/<技能名>/   # 技能本体：README.md（自我介绍）+ SKILL.md + references/
docs/research/           # 技能背后的蒸馏底稿（规范研究工作文件）
SCOPE.md                 # 收录边界
```

## 来源与授权

- 本仓库原创内容以 [MIT](LICENSE) 发布。
