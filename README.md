# collage-infographic

Agent skill for **拼贴感信息图插画（Collage Infographic Illustration）**:
editorial collage that mixes vintage paper media, flat vector, and light pop.

Typical uses: topic covers, blog headers, knowledge explainer art.

## Install

### Grok (this machine, already linked after local setup)

```text
/collage-infographic 帮我画一张关于「注意力」的专题头图
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

- `/collage-infographic`
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
  references/palettes.md
  references/recipes.md
  assets/style-anchor.jpg
```

## License

MIT
