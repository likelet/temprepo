# Super Power Awakening (钞能力觉醒)

This is a funny project for test the agent. 

An A-share investment simulation text adventure game — from 10,000 RMB to stock market mastery.

> Start with 10,000 RMB. Navigate 10 years of real A-share market events. Make every investment decision count.

## How to Play

1. Choose your **investment style** (Technical / Value / Theme Hunter / Zen Investor)
2. A random nickname is generated based on your style
3. Experience **20 randomly selected real A-share market scenarios** (drawn from a pool of 37 events)
4. Make investment decisions at each scenario — choices matching your style earn a **+30% return bonus**
5. Progress through four growth phases: Rookie > Survivor > Awakening > Master
6. Review your investment profile, growth timeline, and leaderboard at the end

### Investment Styles

| Style | Focus | Strengths |
|-------|-------|-----------|
| Technical | Candlesticks / Moving Averages / Volume-Price | Trend following, stop-loss discipline, ETF rotation |
| Value | Financials / Valuation / Margin of Safety | Annual report analysis, contrarian investing, high dividends |
| Theme Hunter | Hot topics / Policy / Event-driven | Concept trading, overseas mapping, speculative plays |
| Zen Investor | DCA / Asset Allocation / Long-term holding | Index DCA, portfolio rebalancing, buy and hold |

### Covered Topics (28 Real A-Share Events)

Bull market mania, thousand stocks limit-down, circuit breaker mechanism, white horse grouping, trade war, convertible bond speculation, hog cycle, fund craze, core asset bubble, rights issue trap, property crisis, MSCI expansion, LPR rate cut, equity pledge explosion, Stock Connect arbitrage, internet antitrust, block trade dump, STAR Market launch, new asset management rules, personal pension, public fund fee cut, New Nine Articles of State Council, PBOC bond buying, Kangmei fraud, limit-up daredevils, delisting crisis, 924 Policy Combo, DeepSeek AI frenzy

## Tech Stack

- Pure HTML + CSS + JavaScript, single file, no external dependencies
- SVG radar chart (investment ability profile)
- localStorage persistent leaderboard
- Hover tooltip system with auto-detected financial terminology (40+ terms)

## Running

Open `index.html` directly in a browser. No server required.

## Changelog

### v7.1 (2026-06-16) — 持仓波动版

- **持仓市场波动**：每个事件开始时，当前持仓根据事件主题产生±1~3.5%的市场波动
- **18种事件主题漂移**：crash事件倾向-1.2%漂移（81%概率亏损），bull事件倾向+0.8%漂移（81%概率盈利）
- **波动视觉反馈**：事件故事前显示📈持仓波动卡片，展示波动百分比和金额
- **时间线记录**：结算面板时间线中以斜体灰色区分波动记录
- **破产可达**：极端情况下波动可导致破产，增加游戏紧张感

### v7.0 (2026-06-16) — 风险博弈版

- **选项随机打乱**：每事件选项显示顺序随机，消除"永远选第一个"元策略
- **风险/回报不对等系统**：每个选项标注🛡️稳健/🎲博弈/🔒保守风险标签，稳健型+3~+12%，博弈型-45%~+18%，保守型-5~+4%
- **仓位管理系统**：每个事件前可选轻仓30%/半仓60%/重仓100%，仓位影响收益绝对值
- **4风格平衡**：蒙特卡洛10000次模拟验证，4风格随机中位收益差距<30%（+52%~+67%）
- **极端爆仓事件**：千股跌停/股权质押/恒大暴雷等事件的最差选项pct低至-45%
- **生产数据**：33事件×4风格×3选项=396个选项，每选项带risk_type属性
- Bumped version to v7.0

### v6.2 (2026-06-16)

- v6.1 风格专属版：每种风格的选项文本完全不同（技术派看K线，价值派看PE，题材猎手追热点，佛系定投）
- 取消通用 style_bonus，改为风格专属选项
- 每次选择后显示当前资产余额
- 银行破产机制：资金归零触发 Game Over
- 端页新增SVG资金曲线图（渐变填充+阶段着色点+收益率标注）
- Bumped version to v6.2

### v6.0 (2026-06-16)

- 银行破产机制上线：资金 ≤ 0 进入破产界面（骷髅动画+随机教训+统计）
- 移除100元下限，允许真正归零
- 版本号更新至 v6.0

### v5.8 (2026-06-16)

- 题库焕新：33个全新事件，叙事升级（对话体/新闻体/心理描写）
- 16/33事件打乱选项风格顺序（不再总是0/1/2/3固定排列）
- 移除打赏二维码
- 四种风格平衡：中位数收益+194%~+234%

### v5.5 (2026-06-16)

- Game renamed to "Super Power Awakening" (钞能力觉醒)
- Added hover tooltip system for key investment concepts
- Added README.md
- Bumped version to v5.5

### v5.6 (2026-06-16)

- README translated to English
- Bumped version to v5.6

- Game renamed to "Super Power Awakening" (钞能力觉醒)
- Added hover tooltip system for key investment concepts: leverage, margin trading, short selling, options, circuit breaker, limit-up/down, ST, registration-based IPO, MSCI, LPR, ETF, convertible bonds, PE/PB/ROE and 40+ more financial terms
- All keywords on the style selection screen are hoverable with explanations
- Event stories and choice texts automatically detect and highlight terminology with tooltips
- Added README.md

### v5.4 (2026-06-16)

- Event pool expanded from 20 to **37 events**, covering 28 real A-share topics
- Added 20 new events: circuit breaker, white horse grouping, trade war, hog cycle, fund craze, core asset bubble, rights issue trap, property crisis, MSCI expansion, LPR rate cut, equity pledge, Stock Connect arbitrage, internet antitrust, block trade, STAR Market, asset management rules, personal pension, fund fee cut, New Nine Articles, PBOC bond buying
- Economic balance optimization: loss option ratio increased from 6.2% to 28%
- Worst-case path adjusted from +126% to -57%; median random path ~+377%
- All four style win rates balanced to ~50%

### v5.3 (2026-06-16)

- Added tip QR code section at game ending
- Added divider and descriptive copy

### v5.2 (2026-06-16)

- Added 17 loss options across 14 events
- Capped extreme profits (bull market event 9500→5500, COVID theme -2500)
- Economic balance: loss rate 6% → 28%

### v5.1 (2026-06-16)

- Random nickname generation system (15 name pool per style)
- Added "reroll" button
- User statistics leaderboard (localStorage, Top 10, max 50 records)
- Gold/Silver/Bronze badges, current game highlighted

### v5.0 (2026-06-16)

- Full rebuild from v4.0
- 4-phase growth system: Rookie → Survivor → Awakening → Master
- Events sorted by timeline (2014–2025)
- Full-screen phase transition animations + HUD progress bar
- SVG radar chart (4 dimensions: Returns / Risk Control / Style / Insight)
- Removed browser extension residual code
- Events expanded from 20 to 27

### v4.0

- Initial version, 20 events
- 4 investment styles + style bonus system
- Basic leaderboard
