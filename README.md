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

### v5.6 (2026-06-16)

- Bumped version to v5.6
- README translated to English

### v5.5 (2026-06-16)

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
