# MJ 真人影视提示词

适用于 **Codex 与 Claude Code** 的同一份skill，专门编写Midjourney图像提示词。默认真人影视、东方仙侠与国风角色、场景及叙事静帧；最终可复制提示词全部使用英文。

## 两种方式

| 方式 | 写法 |
|---|---|
| A：纯提示词 | 由文字交代主体、动作、构图、光色、材质与媒介 |
| B：MJ情绪板／个性化 | 保留画面任务和关键细节，减少参考已承担的风格描述 |

没有选择时先问；已选择的同组迭代不重复问。P码仅使用用户提供的真实配置，不编造代码、不把代码当作强度。

## 本机安装

将本目录整份复制到对应个人skills目录，不要只复制 `SKILL.md`：

- Codex：`~/.codex/skills/mj-cinematic-prompts/`（本机现有个人skills目录；自定义 `CODEX_HOME` 时使用该目录下的 `skills/`）。
- Claude Code：`~/.claude/skills/mj-cinematic-prompts/`。

Windows中的 `~` 指当前用户主目录。若目标已有同名skill，先保留自己的修改再更新。

Codex调用：

```text
$mj-cinematic-prompts
```

Claude Code调用：

```text
/mj-cinematic-prompts
```

也可以说：“使用MJ真人影视提示词skill，纯文字模式，写一座清晨的白玉天宫，空场景，16:9。”

Claude Code个人skill安装路径与斜杠调用方式见[官方文档](https://code.claude.com/docs/en/skills)。已运行的客户端如果未显示新skill，重新打开会话后查看。

## 文件

- [SKILL.md](SKILL.md)：两种模式、提问流程与输出规则，两端共用。
- [画面写法](references/visual-writing.md)：人物、空间、材质、光色与叙事静帧。
- [MJ参数](references/mj-parameters.md)：P码、风格化、版本兼容及官方来源。
- [A/B英文对照](references/mode-examples.md)：三类画面的六条提示词。
- `agents/openai.yaml`：Codex可选展示信息；Claude Code直接读取 `SKILL.md`，无需此元数据。

本skill只组织提示词，不附带MJ账号、API密钥、图片素材或自动出图服务。案例是新写提示词，未进行实际MJ出图验证。
