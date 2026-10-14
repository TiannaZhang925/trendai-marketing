# TrendAI Marketing Agent · AI 新媒体运营技能

一个 [Qoder CLI](https://qoder.cn) Skill：让你的 AI 编程助手变身「企业版 AI 新媒体运营员工」。

每天自动完成内容运营闭环：**实时搜索全网热点 → 结合品牌资料分析匹配机会 → 按平台规范生成营销文案 → AI 生成配图 → 四维策略评分与优化建议。**

## 功能

| 能力 | 说明 |
| --- | --- |
| 📰 今日热点 Top 10 | WebSearch 实时抓取微博/抖音/TikTok/Google Trends/Reddit/行业新闻/AI 资讯，输出热度、增长趋势、用户情绪、商业关联度与品牌匹配度排序，每个热点附 2 个可执行玩法方向 |
| ✍️ 平台定制文案 | 小红书（爆款标题×5+种草正文+标签）、抖音/TikTok/Reels（3 秒 Hook+分镜脚本+CTA）、LinkedIn（趋势-痛点-方案-价值洞察文）、微信公众号、Instagram/X |
| 🎨 AI 配图 | 自动生成英文图片 Prompt（封面图/产品宣传图/信息图），调用 ImageGen 按平台尺寸出图（3:4 / 9:16 / 16:9） |
| 📊 内容评分 | 热点相关性、品牌匹配度、传播潜力、转化可能四维 0-100 + 综合「🔥爆款概率」+ 一条可执行的优化建议 |
| 🏢 品牌档案 | 企业信息、卖点、调性、目标平台一次设置、全局复用，所有产出自动贴合品牌语境 |

## 安装

**方式一：克隆到用户级技能目录（所有项目可用，推荐）**

```bash
git clone https://github.com/<你的用户名>/trendai-marketing.git \
  ~/.qoder-cn/skills/trendai-marketing
```

**方式二：项目级**——把本目录复制到项目的 `.qoder/skills/trendai-marketing/`。

**方式三：手动下载**——点击 Code → Download ZIP，解压后将整个文件夹放入上述任一目录。

安装后重启会话或运行 `/skills reload`，用 `/skills list` 确认技能已加载。

## 使用

```
/trendai-marketing setup          # 首次：填写品牌资料（企业/行业/卖点/调性/平台）
/trendai-marketing today          # 今日热点分析与推荐机会 Top 10
/trendai-marketing create 小红书   # 选最匹配热点，按平台规范生成文案并评分
/trendai-marketing image          # 生成营销配图
```

也可以直接说自然语言：「看看今天追什么，帮我写成小红书笔记并配图」——技能会自动串联全流程，成品输出到当前目录 `trendai-content/`。

## 目录结构

```
trendai-marketing/
├── SKILL.md                          # 技能主流程与模式路由
├── references/
│   ├── trend-research.md             # 7 类数据源检索配方与热点筛选标准
│   ├── platform-playbooks.md         # 各平台内容结构与文风规范
│   └── scoring-rubric.md             # 匹配度与爆款概率评分口径
└── brand/
    └── brand-profile.md              # 品牌档案（setup 时生成，本地私有数据）
```

## 注意事项

- 热点数据来自实时网络搜索，热度指数为相对估算；发布前请人工复核内容。
- `brand/brand-profile.md` 是你的私有品牌数据；若 fork 后公开使用，注意不要提交真实资料。
- 生成的营销图片仅供发布参考，商用时请确认所平台对 AI 内容的标注政策。

## License

MIT
