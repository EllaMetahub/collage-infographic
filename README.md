# collage-infographic

Agent skill for **拼贴感信息图插画（Collage Infographic Illustration）**:
editorial collage that mixes vintage paper media, flat vector, and light pop.

Typical uses: topic covers, blog headers, knowledge explainer art.

## Install

### Grok (this machine, already linked after local setup)

```text
/collage-infographic 「拼贴感信息图插画（Collage Infographic Illustration）」，同时混合了一点 复古纸媒 + 扁平矢量 + 轻波普元素 的方向。可以理解为一种 “编辑式插画风”，常见在专题封面、博客头图、知识型内容配图里。
核心特征

拼贴构成（Collage）

   * 人物、物件、纹理像剪下来再重新组合
   * 有明显的“贴上去”的层次感，而不是完整场景透视

纸媒/印刷质感

   * 颗粒、噪点、做旧纹理（像杂志扫描）
   * 类似报刊、百科页、专栏配图的气质

扁平化 + 轻几何

   * 轮廓干净、颜色块明确
   * 不追求真实光影，更偏“概念表达”

信息可视化思维

   * 放大元素（放大镜、箭头、符号、图形）
   * 更像是在“解释一个观点”，而不是讲故事

高对比限定配色

   * 常用蓝 / 紫 / 橙 / 米色这种编辑感配色
   * 颜色不多，但识别度强
```

### From GitHub

Repo: [EllaMetahub/collage-infographic](https://github.com/EllaMetahub/collage-infographic)

**Grok plugin**

```bash
grok plugin marketplace add EllaMetahub/collage-infographic
grok plugin install collage-infographic --trust
```

Or install the repo directly:

```bash
grok plugin install EllaMetahub/collage-infographic --trust
```

**Copy as a user skill**

```bash
git clone https://github.com/EllaMetahub/collage-infographic.git
# Grok
cp -r collage-infographic/skills/collage-infographic ~/.grok/skills/collage-infographic
# Claude Code
cp -r collage-infographic/skills/collage-infographic ~/.claude/skills/collage-infographic
# Cursor
cp -r collage-infographic/skills/collage-infographic ~/.cursor/skills/collage-infographic
```

**npx skills** (if you use the Agent Skills CLI)

```bash
npx skills add EllaMetahub/collage-infographic
```

## Use

Fastest way for any AI tool — paste this:

```text
用这个 skill：https://github.com/EllaMetahub/collage-infographic
按里面锁定的风格提示词生图，标题：【这里写标题】
```

Example:

```text
用这个 skill：https://github.com/EllaMetahub/collage-infographic
按里面锁定的风格提示词生图，标题：
```

Installed locally:

- `/collage-infographic 标题：`
- Or just ask: 画一张拼贴感信息图 / editorial collage infographic of …

The agent should:

1. Explain **one** viewpoint visually
2. Build cut-out paper layers (not a 3D scene)
3. Keep grainy print texture + flat color blocks
4. Use cobalt / violet / tangerine / beige unless you name another palette

## Repo layout

```
plugin.json
.grok-plugin/marketplace.json
skills/collage-infographic/
  SKILL.md
  references/style-prompt.md   # locked 生图提示词（原文）
  references/palettes.md
  references/recipes.md
  assets/style-anchor.jpg
```

## License

MIT
