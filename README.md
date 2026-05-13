# JR Academy / 匠人学院 — Master Brand Book

> **学 AI 来匠人 · STUDY AI AT JR ACADEMY**
> 一起成为 AI 时代的匠人 · Be an AI Craftsman.
>
> 专业的 AI 学习平台 · 课程 · 实战 · 就业
>
> ---
>
> 🌐 **在线手册**: <https://jr-academy-ai.github.io/jr-academy-brand/>
>
> 总品牌 UI 规范 / 品牌手册，不是产品代码。双击 `index.html` 就能看，或直接访问上面的在线版本。
> JR Academy 是母品牌，UniMate AI / Cert Master / Job Hunter 是子品牌。

---

## 目录结构

```
jr-academy-brand/
├── index.html              ← 品牌手册（10 sections，双击打开就能看）
├── DESIGN.md               ← 完整设计规范（13 节）
├── _source_design.md       ← 原始设计研究稿（存档）
├── tokens/
│   ├── tokens.json         ← Design tokens 源数据（W3C 格式）
│   └── tokens.css          ← CSS Variables（--jr-*），任何项目 import 即可用
└── assets/
    ├── logo/               ← Logo 5 件套（TODO — logo 还在设计中）
    ├── mascot/             ← 牛小匠 11 视图 + 8 动作（TODO）
    ├── illustrations/      ← 4 大场景插画（探索方向 / 提升能力 / 链接机会 / 成长未来）
    ├── banners/            ← Hero banner / 推广 banner
    └── _inbox/             ← 待分类
```

---

## 用法

### 看规范
双击 `index.html`，10 个 section：
Colors / Typography / Dashboard / Mobile / Components / Inputs / Alerts / Toast / Illustrations / Mascot IP + Design Principles.

### 读设计决策
`DESIGN.md` — 完整 13 节规范，包含：
- 品牌定位（母品牌 vs 三个子品牌）
- 牛小匠 IP 详解（11 视图 + 8 动作）
- 用色决策树
- 组件规范
- Voice & Tone
- **四品牌隔离规则**

### 在产品里用 tokens

```css
@import url('path/to/jr-academy-brand/tokens/tokens.css');

.cta-primary {
  background: var(--jr-coral);
  color: white;
  border-radius: var(--jr-radius-sm);
  box-shadow: var(--jr-glow-red);
  padding: 0 var(--jr-space-6);
  height: 48px;
  font-weight: 700;
}

.progress {
  background: var(--jr-purple); /* 学习进度用紫，不要用 Coral */
}
```

CSS 前缀 `--jr-*` 跟 `--um-*` / `--cm-*` / `--jh-*` 完全隔离，四个品牌可同 import。

---

## 品牌 DNA（一句话）

> **AI 时代的全球华人学习陪伴品牌** — 不是普通教育平台 UI，而是有明确 IP 记忆点的 AI 学习陪伴型品牌系统。

四条不可妥协：**Coral Red CTA · 牛小匠红 JR 连帽衫 + 墨镜 + JR 胸标 · JR Box 视觉资产 · 白/Mist Gray 大底**。

---

## 子品牌生态

```
JR Academy (匠人学院 · 母品牌)    ← 本仓库
├── UniMate AI / 牛小匠课代表    — 大学生学习陪伴
├── Cert Master / 考证匠         — 考证 (注会 / 一建 / 法考)
└── Job Hunter / 求职匠          — 求职 (JD 分析 / 简历 / 面试)
```

总品牌 ↔ 子品牌的隔离规则见 `DESIGN.md §13`。

---

## 红线（看到立即打回）

- ❌ 大块 bg 用 Coral Red（CTA 专属）
- ❌ Royal Purple 当主 CTA（紫是 AI / 信息标识）
- ❌ 蓝色作主 CTA（那是 Job Hunter 子品牌的）
- ❌ 牛小匠去掉墨镜 / 红衣 / JR 胸标
- ❌ 一屏用两套不同 outfit 的牛小匠
- ❌ 旧吉祥物 + 牛小匠混用
- ❌ "您 / 智能化 / 宝子"

---

## 牛小匠 11 视图

Front · Side · Back · Sitting · Laptop · Tablet · Wave · Like · Thinking · Teaching · Celebration

## 高频 8 动作

开心 · 思考 · 点赞 · 讲解 · 努力 · 庆祝 · 疑问 · 加油

---

## 待补 (TODO)

- [ ] Logo 5 件套（JR Box / 横版 / 紧凑 / Avatar / App Icon）— **正在设计**
- [ ] 牛小匠 11 视图（front / side / back / sitting / laptop / tablet / wave / like / thinking / teaching / celebration）
- [ ] 4 张大场景插画（探索方向 / 提升能力 / 链接机会 / 成长未来）
- [ ] Style Dictionary 配置 — 输出 Tailwind preset / iOS / Android

---

## Deploy

GitHub Pages auto-deploy via `.github/workflows/deploy.yml` — push to `main` 自动构建发布。

- **在线访问**: <https://jr-academy-ai.github.io/jr-academy-brand/>
- **Repo**: <https://github.com/JR-Academy-AI/jr-academy-brand>

---

## 维护

- 源 spec 图：放 `assets/mascot/spec-sheet.png`
- 原始设计稿：`_source_design.md`
- 最近更新：2026-05-13

任何 token 改动**三处同步**：`DESIGN.md` → `tokens.json` → `tokens.css`。
冲突时以 `DESIGN.md` 为准。
