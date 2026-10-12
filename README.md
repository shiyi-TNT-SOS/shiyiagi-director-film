# shiyiagi-director-film · 故事片 AI 视频导演提示词

> 把「AI 扮演故事片导演」从口号固化成可复用的提示词结构。专治片子「漂亮但空洞、镜头不推进、情绪不到位、人物不立体」。

## 它解决什么

故事片最容易翻车的是"**漂亮但空洞**"——AI 能产出唯美镜头，但镜头之间不推进、情绪落不到人身上。本 skill 提供两层，按需取用：

- **轻量层**：四要素（目标 / 素材 / 规格 / 边界）+ 戏剧功能骨架 → 直接出分镜。适合单场戏、单镜、短视频。
- **深度层**：人物弧光 + 三幕结构 + 晚进早出 + 潜台词 → 先立人物与结构，再分镜。适合短片 / 有完整人物变化的片子。

## 核心方法

- **戏剧功能挂靠**：每镜必须推进叙事或人物，否则删。
- **情绪镜头语法**：情绪值 ↔ 镜头参数映射（1–5），静默节点（释放型用"静"、爆发型用"满"）。
- **视觉母题呼应**：一个意象贯穿全片，承载主题。
- **概念转译法**：情绪词（孤独 / 温暖 / 压抑 / 释然 / 荒诞 / 怀旧）→ 镜头 / 构图 / 运镜 / 光线 / 色彩 五类元件。

## 交付物

- **导演提示词** → 喂给 LLM，产出分镜表与逐镜提示词
- **单镜头生成提示词** → 喂给视频模型（即梦 / 可灵 / Seedance / Grok）出片

## 目录结构

```
shiyiagi-director-film/
├── SKILL.md
├── README.md
└── references/
    ├── story-director-prompt.md    # 主模板（四要素契约）
    ├── narrative-structure.md       # 人物弧光 / 三幕 / 潜台词 / 晚进早出
    ├── emotion-shot-design.md       # 情绪镜头设计层（情绪值↔参数）
    ├── concept-translation.md       # 情绪词五类元件转译
    ├── ai-video-prompt.md           # 七段顺序铁律
    ├── lens-grammar.md              # 镜头语法七维
    ├── compliance.md                # 合规边界
    ├── production.md                # 生产层结论
    ├── platform-specs.md            # 引擎规格
    ├── style-anchors.md             # 风格锚点
    ├── troubleshooting.md           # 常见翻车与修复
    └── walkthrough-film.md          # 60s 短片"夜归"孤独→释然 端到端示例
```

## 怎么用

1. 把 `SKILL.md` 作为指令交给 LLM。
2. LLM 按流程产出：叙事结构（轻量 / 深度）→ 分镜表 → 逐镜提示词。
3. 把逐镜提示词喂给视频模型出片。

## 适用 / 不适用

- ✅ 电影感短片、故事片、叙事向分镜、情绪向镜头、人物弧光
- ❌ 武打 / 格斗 / 动作戏 → `shiyiagi-director-action`
- ❌ 品牌形象片 → `shiyiagi-director-ad-tvc`
- ❌ 剧情带货（要转化 / CTA） → `shiyiagi-director-story-selling`

## 版本与授权

- 版本：**v1.4.0**
- 作者：十一AGI（柳十一 / 十一AGI认知圈）
- 授权：学习与非商业用途可自由使用；商用请先联系作者授权。

## 系列导航

| Skill | 定位 |
|---|---|
| [shiyiagi-director-ad-tvc](https://github.com/shiyi-TNT-SOS/shiyiagi-director-ad-tvc) | 品牌广告片 / TVC / 形象片 |
| **shiyiagi-director-film（本仓库）** | 故事片 / 叙事短片 |
| [shiyiagi-director-story-selling](https://github.com/shiyi-TNT-SOS/shiyiagi-director-story-selling) | 剧情化带货短视频（独立付费发布线） |
| [shiyiagi-director-action](https://github.com/shiyi-TNT-SOS/shiyiagi-director-action) | 武打 / 格斗 / 动作戏 |
