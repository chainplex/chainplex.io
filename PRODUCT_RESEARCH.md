# ChainPlex.io — Product Research & Customer Needs

_Last updated: 2026-03-23_

---

## 🎯 Target Market

ChainPlex is positioning as **the investor-friendly TAO analytics platform** — filling the gap between TaoStats.io (too technical) and nothing (no good investor dashboard exists).

**Two user segments:**

| Segment | Profile | Primary Need |
|---|---|---|
| **Investors** | Holds or considering TAO, not technical, wants ROI clarity | Price context, staking yield, "is now a good time?" |
| **Builders/Miners** | Running subnets/validators, technical | Subnet performance, emission data, competition |

**Priority focus: Investors** — TaoStats.io already serves builders. Nobody serves investors well.

---

## 📊 Customer Research — Reddit r/bittensor_ (March 2026)

### Top Questions & Needs (by engagement)

**1. Mainstream credibility signals** ⬆️73 upvotes
- Chamath Palihapitiya discussed Bittensor/Templar (SN3) on All-In Podcast with Jensen Huang
- Covenant-72B training run cited — first mainstream tech podcast coverage at this level
- **Need:** Page tracking TAO mainstream media mentions, partnerships, institutional interest

**2. Staking confidence** ⬆️18 upvotes
- "76% of TAO is staked — highest of any crypto"
- People sharing this as bullish signal
- **Need:** Live staking dashboard — % staked, APY by validator, total staked TAO, staking calculator

**3. Investment thesis explanation** ⬆️high engagement
- Coase/Hayek framing: TAO solves OpenAI's "calculation problem"
- 129 subnets with market caps = price signals centralized AI lacks
- Subnet 64 (Chutes) = $91.8M cap vs Subnet 110 = $0.77 — market allocating AI resources
- **Need:** Visual explainer of TAO's economic thesis + subnet market cap comparison

**4. "Am I early?" framing**
- "TAO at 0.95% of $300B AI market — Bitcoin is 53% of crypto market"
- If TAO hits 10% of AI market = 10x from current
- **Need:** TAO market cap vs AI industry market size visualization

**5. Entry point questions**
- Constantly asked: "Is now a good time to buy?"
- **Need:** On-chain metrics to contextualize price (similar to BTC MVRV but for TAO)

---

## 🏆 Competitive Landscape

| Platform | Strength | Weakness |
|---|---|---|
| TaoStats.io | Raw blockchain data, validators, staking | Ugly UI, too technical for investors |
| Messari | Professional research | No TAO-specific depth, expensive |
| CoinGecko/CMC | Price data | No on-chain depth |
| Nothing | — | Clean investor-friendly TAO analytics |

**ChainPlex opportunity:** The clean, modern, investor-focused TAO analytics layer on top of public data.

---

## 🔥 Priority Features (ranked by community demand)

### P0 — Build First (Viral Potential)

**1. Subnet Market Cap Leaderboard**
- Sortable table: all 129+ subnets with market cap, 24h change, emission %, description
- Filter by category (text, compute, storage, finance, vision)
- Click subnet → detail page
- _Why viral:_ Nothing like this exists. Every TAO discussion references subnets without data.
- _Data source:_ TaoStats.io API (free)

**2. TAO Staking Calculator**
- Input: TAO amount → Output: estimated monthly/yearly yield
- Show: current APY range (15-20%), best validators, minimum stake
- _Why needed:_ #1 question from investors — "what do I earn?"

### P1 — High Value

**3. TAO vs Centralized AI Narrative Page**
- Visual: TAO market cap vs OpenAI/Google AI revenue
- The Coase calculation problem explained simply
- "If TAO captures X% of AI market = $Y per TAO"
- _Audience:_ Investors who need the thesis visualized

**4. TAO Mainstream Tracker**
- Feed of notable TAO mentions: podcasts, news, institutional interest
- Chamath/All-In, Goldman Sachs reports, etc.
- Auto-updated via web scraping

**5. Live Staking Dashboard**
- Total TAO staked (live from chain)
- % of supply staked vs historical
- Top validators by stake + APY
- Your stake tracker (input wallet address)

### P2 — Nice to Have

**6. TAO Price Contextualization**
- Custom scoring: "Is TAO cheap or expensive right now?"
- Based on: staking ratio, subnet activity, price vs ATH
- Simple buy/hold/wait signal for investors

**7. New Subnet Tracker**
- Recently launched subnets
- Registration burn events (deflationary signal)
- Subnet graduation metrics

**8. TAO vs BTC Correlation**
- Does TAO move with BTC or independently?
- When does TAO decouple? (AI news events)

---

## 🏗️ Tech Decisions

### Current Stack (Phase 1)
- Plain HTML/CSS/JS + Plotly.js
- GitHub Pages hosting (free)
- CoinGecko + Kraken APIs (free)

### Upgrade Path (Phase 2 — when there's traction)
- **Next.js** — component system, proper routing, professional feel
- **TaoStats.io API** — real subnet data
- **Supabase** — user accounts, saved portfolios, alerts
- **Vercel** — better hosting with SSR

### Why not rebuild now?
Ship P0 features first. Validate there's user demand. Then rebuild properly.

---

## 📈 Go-to-Market Strategy

**Step 1: Build the Subnet Leaderboard (1-2 days)**
- First truly useful TAO feature
- Post it in r/bittensor_ with "I built this because nothing like it exists"

**Step 2: Post on @chainplexio X account**
- Screenshot of leaderboard with data
- Tag @opentensor, @tplr_ai, key validators

**Step 3: Share in Bittensor Discord**
- #general and #subnet-specific channels
- "Here's how your subnet ranks vs others"

**Target:** 500 engaged users before monetizing anything

---

## 💰 Monetization (Later)

- **Free:** Core analytics, price, subnet leaderboard
- **Pro ($9-29/mo):** Price alerts, wallet tracking, staking optimizer, API access
- **API tier:** For validators/builders who want to query data

---

## 📝 Open Questions

1. Does TaoStats.io have a public API we can use? (Need to verify terms)
2. Is there a Bittensor Discord we should join to validate ideas?
3. Should we niche down further to just TAO, or keep BTC/SOL/HYPE for SEO breadth?
4. What's the best way to get subnet market cap data without a paid API?

---

_This document is a living product brief. Update as we learn more._
