# 去油去脏写法（默认）

真人方向的提示词默认都按本文件写，A、B 两种方式都适用。用户的 MJ 图大多要进 H3、Seedance 做视频：静帧里看着是「质感」的东西，进了视频会变成脏和油。

## 为什么要这样写

2026-11-04 对比过两组情绪板：「港风」（浅景深人像、胶片柔光、中间调偏暖）进 H3 质感好；「疯人院」（碎纹理多、湿地面和亮瓷砖多、中间调偏绿、前后全清楚）静帧还行，进 H3 就脏、就油。原因有四条，写词时一一避开：

1. **碎纹理**：掉漆、锈斑、裂缝、碎玻璃、满天碎屑。视频每帧都要重画这些细节，画不稳，就闪、就糊成噪点，看着脏。
2. **湿亮反光**：汗湿的皮肤、湿地面、亮瓷砖、油彩。镜头一动反光就跟着滑，还会被套到皮肤上，看着油。
3. **中间调偏绿或偏青**：肤色就在中间调。冷绿的光铺到脸上，人就发青发灰，像菜色、脏脸。
4. **前后全清楚、CG 感**：没有虚化帮忙遮瑕，背景的细节跟脸抢；CG 特效感会把整段视频往 CG 方向带。

这是看图加数据得出的判断，还没逐条做过视频 A/B 验证。

## 什么时候用、什么时候让步

- 默认：所有真人方向的人物静帧、空场景、特写都用。
- 用户点名要湿、脏、血、反光（雨夜、泥战、血战）：照写，但用下面「局部、写位置、写成干的或哑光」的写法；块外用一句话提醒这是进视频最容易发油发脏的地方。
- 用户说不要颗粒、要干净的画面时，以用户为准。
- 多视图资料图、三视图：不加浅景深，按下文的「定妆／资料图」尾句写。

## 写法：短句、固定顺序

用短句和逗号分组，可以省掉 a/the，一个细节一个短语。顺序固定为：

**景别 + 地点／时间 + 背景虚化 → 人物（国籍、性别、年龄、体型、脸型）→ 画面位置和朝向 → 动作和表情 → 五官细节 → 皮肤质感 → 头发 → 伤、妆、汗 → 服装 → 光（主光从哪来，冷色只做细边光）→ 背景元素（少、大、虚）→ 质感尾句 → 媒介锚点 → 参数**

压缩时**不能丢**这几样：
- 朝向：`facing the camera`、`three-quarter back view` 等。
- 左右：身体的左右和画面的左右都要写，例如 `cut on left forehead, frame right`。不写清楚，MJ 会把伤口、记号画到另一边。
- 人数、动作停在哪一刻（要当视频首帧时写动作开始前，见 [给视频当首帧](video-first-frame.md)）。
- `--ar` 和其他参数。

## 样板（用户 2026-11-04 认可的写法）

```text
Chest up close shot, burning city street at night, flames and buildings blurred behind him. Thin, handsome Chinese man, late twenties, gaunt hollow cheeked face, slightly left of center, facing the camera, head thrust forward, roaring mouth wide open, teeth bared, neck tendons straining, eyes wide and blazing. Sharp jaw, thick straight dark brows, light stubble, matte tan skin with gray ash on cheekbone and brow, damp messy black hair whipping across forehead. Red cut with dried blood on left forehead, frame right. Worn pale gray beige striped cotton shirt hanging open at chest. Warm orange firelight from frame left; thin cyan rim light from frame right tracing cheek and jaw edge. Large blurred insect silhouettes with faint green glints in smoke behind him. Shallow depth of field, face in sharp focus, muted palette, fine 35mm film grain. Live action Chinese sci fi action film still --ar 16:9
```

## 替换表

| 别这样写 | 改成 | 说明 |
|---|---|---|
| sweat-slick, glistening, oily, glossy skin, dewy | `matte skin`, `dry matte skin`；要汗就写 `a few beads of sweat at the temples` | 汗只落在一处，不铺满脸 |
| wet hair, soaked, drenched | `damp hair in heavy clumped strands`；衣服写 `rain-darkened matte cotton/linen` | 保留湿的形状（成绺、变重、颜色变深），去掉反光 |
| dirty, grimy, filthy, stained, smeared with … | `worn`, `faded`, `a light dusting of ash/dust on [具体位置]` | 脏只落在一两处，写清在哪 |
| raw / fresh / bleeding gash, dripping blood | `red cut with dried blood at its edges` | 干的血不反光 |
| greasepaint, glossy makeup, lip gloss | `chalky matte face paint`, `matte makeup` | greasepaint 字面就是「油彩」 |
| rusted, chipped paint, peeling, cracked, crumbling | `dull painted`, `worn smooth`；只留大形状（铆钉、栏杆、门框），并让它虚掉 | 碎纹理换成大块面 |
| wet floor, puddles, polished / reflective floor, glazed tiles | `dry concrete floor`, `matte floor`；一定要雨地时写 `rain-darkened matte ground, a few soft dull reflections` | 反光要少、要钝 |
| crowd, swarm, countless, flying debris, particles everywhere | `a few large blurred …` | 又多又小的东西进视频最容易闪 |
| sickly, pale greenish skin | `gaunt, hollow-cheeked`（用脸型表现病态） | 不让肤色往青绿走 |
| 半边脸铺青光、绿光 | 主光暖色或中性；冷色只写成 `thin cyan rim light tracing cheek and jaw edge` | 中间调保持偏暖 |
| neon / fluorescent green glints | `faint green glints` | 少、淡 |
| heavy grain, gritty, grainy, noisy | `fine 35mm film grain` | 颗粒要细；粗颗粒本身就是碎纹理 |
| 只写 dramatic lighting、hard light 铺满全脸 | 写光的来源和方向；需要读清脸时写 `falls softly and evenly across his face` | 硬光打在皮肤上全是亮斑 |

情绪板明显偏冷、偏绿时，人物皮肤加一句 `natural warm undertone`。

## 质感尾句（按画面类型）

| 画面类型 | 尾句 |
|---|---|
| 人物近景、中景静帧 | `Shallow depth of field, face in sharp focus, muted palette, fine 35mm film grain.` |
| 道具、手部特写 | `Shallow depth of field, [the object] in sharp focus, muted palette, fine 35mm film grain.` |
| 空场景、大场景 | `Soft atmospheric depth, distant layers softened by haze, muted palette, fine 35mm film grain.`（不硬加浅景深；前景材质写大形，不写碎纹理） |
| 定妆、资料图 | `Even soft light, matte skin and fabric, fine 35mm film grain.`（不加浅景深） |

想让颗粒更明显时，写 `visible fine 35mm film grain`，不要换成 heavy 或 gritty。

尾句后面接一条媒介锚点，例如 `Live action Chinese sci fi action film still`，最后放参数。

## B 方式也保留

情绪板负责大致审美，但「疯人院」这类情绪板本身就带着油和脏。所以质感短语（matte、damp、dried blood、a few …）和质感尾句**不算重复风格，B 也要保留**：它们是用来压住情绪板的。人物静帧这样写，常到 90–140 个英文词，属正常。

去油去脏后还是太脏时，提示词先别动，下一轮只把 `--s` 调低一点（让情绪板少压一点），一次只改一处。

## 自检

- 替换表左边那一列的词，块内一个都没有（用户点名要的除外，块外已提醒）。
- 皮肤写了 matte；汗、湿、脏、血都只落在具体的一两处。
- 冷色光只做细边光或小面积背景，没有铺满半张脸。
- 背景元素少、大、虚。
- 有质感尾句，有媒介锚点，有 `--ar`。
- 朝向、左右、画面位置没在压缩中丢掉。
