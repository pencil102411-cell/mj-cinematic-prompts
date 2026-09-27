# 同题A/B对照

这些是新写示例，未做MJ出图测试，不是来源博主的原提示词。供校准保留与精简的边界，平时只向用户输出其选择的模式。以下B均假设用户已在MJ选好相符的情绪板／个性化，因此省略P码；用户给出真实代码时再添加。

## 1. 角色定妆：山门执事

### A：文字建立角色、光材与审美

```text
Full-body costume portrait of a Chinese female mountain-sect steward in her early thirties, slightly angular face, straight brows, black hair in a low knot. Layered ivory linen robes beneath a muted blue silk coat, a narrow brown leather belt, one worn bronze key hanging at her waist. Upright relaxed posture, both hands visible, head and feet fully in frame. Plain warm-gray plaster background, soft window light from the left, gentle shadow detail, natural skin texture, distinct linen fibers and restrained silk highlights. Grounded live-action Chinese fantasy costume photography --ar 2:3
```

### B：删总体风格铺陈，保留资产辨识与可读性

```text
Full-body portrait of a Chinese female mountain-sect steward, angular face, straight brows, low black hair knot. Ivory linen robes, muted blue silk coat, brown belt, bronze waist key. Upright relaxed posture, visible hands, head and feet fully in frame, plain background, soft readable light, live-action costume photography --ar 2:3
```

比例来自全身角色展示需求，不是把本skill横屏默认硬套到所有资产图。

## 2. 空场景：云海测候台

### A：空间、材料、天气与光色都由文字定义

```text
An unoccupied celestial observatory above a low sea of clouds, wide view through a dark stone doorway. A narrow dry walkway crosses the rain-soaked pale limestone terrace toward three massive bronze astronomical rings. Fine mineral veins, localized green patina, damp hemp ropes, shallow puddles reflecting the rings. Distant mountain ridges emerge through layered mist. Cool gray and celadon dominate, with a narrow band of warm dawn light crossing the terrace from the right. Clearly readable foreground, middle ground and distance, monumental architecture with tactile physical construction, live-action Chinese fantasy production still --ar 16:9 --no people
```

### B：保留空间与无人的要求，减少色材修饰

```text
Unoccupied celestial observatory above a cloud sea, framed by a dark stone doorway. A narrow walkway crosses a wet limestone terrace toward three enormous bronze astronomical rings, shallow reflections below, distant misty mountains, soft dawn light. Monumental scale, tactile architecture, live-action Chinese fantasy film still --ar 16:9 --no people
```

不可把B缩成“beautiful celestial palace”而丢掉观看入口、路径和主体。

## 3. 叙事静帧：交还令牌

### A：给一个动作完整的观看关系

```text
An over-the-shoulder medium close-up of a young Chinese swordswoman returning a worn bronze token to an elderly gatekeeper. Her open right palm holds the token between them, his reaching hand stopping just short of hers. Rain-darkened blue-gray linen robes, a loose black hair strand against her cheek, lowered eyes and a tightly held jaw. The gatekeeper's brown shoulder is softly blurred in the foreground, an old timber doorway and pale mountain mist behind her. Cool overcast daylight with gentle stone-wall bounce, visible palm lines and damp cloth weight, restrained live-action wuxia drama still --ar 16:9
```

### B：动作、关系、观看位置与情绪仍不可删

```text
Over-the-shoulder medium close-up of a Chinese swordswoman returning a bronze token to an elderly gatekeeper, their hands almost touching. Damp blue-gray linen robes, loose black hair, lowered eyes, tense jaw. His blurred shoulder in the foreground, timber mountain gate behind her, soft overcast light, live-action wuxia film still --ar 16:9
```

## 交互示例

- 用户：“写一个真人仙侠场景，用MJ。” → 只先问两种方式；不擅自给A成品。
- 用户：“纯文字，云上的白玉宫殿，画面不要人。” → 直接A；不再问模式，不自动加P或小人物。
- 用户：“用我已经选好的情绪板，写一个红衣女侠雨中回头，不用填P码。” → 直接B，短而具体；代码块不出现虚构ID。
- 用户：“刚才的情绪板继续，改成全景。” → 沿用B与已知参考条件，仅调整景别和空间，不重复模式提问。
- 用户：“P值调到500。” → 若上下文不能确定是代码还是强度，先辨明含义，不自动造参数。
- 用户：“人物脸每张都不一样，把P加大就行吗？” → 说明P控制审美倾向，不承担锁脸；检查资产描述与所用版本的适用参考功能，不承诺加P解决。
- 用户：“纯文字，只把晴天白衣女子窗边读书这段转成英文，动作和衣服别改。” → 忠实转译已有画面；不主动加剑、雨、悲伤故事或夜灯。
- 用户：“继续用情绪板，把这张竖版回眸半身照改成16:9，保留表情。” → 保留半身和表情，重新安排人物位置及横向视线空间；不只换比例，不缩成远处小人。
- 用户：“情绪板只借光色，我的角色不戴头巾，是高髻。” → 明写高髻；不将参考中的头巾并入通用人物模板。若实际生成仍出现头巾，再检查参考影响，不许诺文字一定覆盖它。
- 用户：“把已有A版改短，我用了情绪板；黑衣在亮窗前这个关系必须留。” → 保留人物对亮背景的明暗分离，优先删总体调色和重复电影质感标签。
