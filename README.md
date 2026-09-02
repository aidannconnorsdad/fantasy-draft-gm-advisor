# ⚡ Fantasy Draft GM Advisor

**A single, self-contained 2026 NFL fantasy football draft companion** — multi-source ADP comparison, positional scarcity alerts, and richer GM-style insight notes, all in one static HTML page.

Built for serious fantasy managers who want data-driven draft decisions in a high-speed draft-day environment.

---

## What this tool is (and isn't)

**It is:**
- A **single consolidated advisor** — one `index.html` file plus one data file, no separate tools or backends to juggle.
- A **live draft-day tracker**: log picks as they happen and get updated recommendations instantly.
- A **decision-support layer**: multi-source ADP, positional scarcity alerts, and GM insight notes (workload security, offensive environment, coaching/scheme impact, contract outlook, injury durability, competition for touches, and breakout/decline signals) to help you weigh a pick beyond raw rankings.

**It is not:**
- A trade simulator — it doesn't predict other teams' picks or optimize post-draft trades.
- A live-syncing app — there's no backend or API; you log every pick manually.
- A guaranteed source of truth — GM insight notes are directional draft-prep context, not verified real-time reporting. **Refresh player and GM insight data before draft day** (see [Keeping data fresh](#-keeping-data-fresh) below), since injuries, depth charts, and contract situations can change quickly during the preseason.

---

## 🚀 Quick Start

### Before Draft (5 minutes)

1. **Download the tool:**
   - Click the green `<> Code` button on this GitHub page
   - Select "Download ZIP"
   - Unzip the folder anywhere on your computer

2. **Open the dashboard:**
   - Find `index.html` in the unzipped folder
   - Double-click it (opens in your browser)
   - Test it—you should see player data loading

3. **Have it ready:**
   - Keep the browser tab open
   - Use on phone, tablet, or laptop during draft
   - Bookmark it for quick access

### During Draft (1-minute clock)

1. **Log each pick (yours and others):**
   - Pick # (1, 2, 3, etc.)
   - Team Name
   - Player Name (type to see suggestions)
   - Position (QB, RB, WR, TE, FLEX, K, DEF)
   - Click "Log Pick"

2. **Read the recommendations:**
   - Top 12 available players ranked by value
   - Multi-source ADP (FantasyPros, Yahoo, ESPN, DraftKings)
   - GM insight notes: workload security, offensive environment, coaching/scheme impact, contract outlook, injury durability, competition for touches, and breakout/decline signal
   - Risk assessment (Low/Medium/High)

3. **Watch for alerts:**
   - **Positional Scarcity:** When elite RBs run out, it flags it
   - **ADP Variance:** Spots undervalued players (shop alerts!)
   - **Your Roster:** Real-time stats on RB/WR depth

---

## 📊 Understanding the Dashboard

### Your Roster (Left Panel)
- **Picks:** Total picks made
- **RB Count / WR Count / Other:** Position breakdown
- **Roster List:** All your picks so far

*Why it matters:* Helps you identify gaps. If you have 0 RBs after round 4, you need to react.

---

### Positional Scarcity (Right Panel)
Three alert levels:

| Alert | Meaning | Action |
|-------|---------|--------|
| 🚨 **CRITICAL** | Elite RBs nearly gone | Grab one NOW if needed |
| ⏰ **WARNING** | Position getting thin | Plan to draft next 1-2 rounds |
| ✅ **INFO** | Plenty available | You can wait |

*Why it matters:* You'll know when to abandon your strategy. If 8 teams need RB and only 3 are left, you reach or miss out.

---

### Next Best Available (Center Panel)
Shows top 12 available players with:

#### Consensus ADP
```
FP: 1.2 | Yahoo: 1.3 | Consensus: 1.25
```
- **FP** = FantasyPros (expert aggregate)
- **Yahoo** = Your league platform
- **Consensus** = Average of all sources

#### ADP Variance (Shop Alert!)
If one source rates a player way different:
- ✅ Player ADP 10 on FantasyPros, ADP 14 on Yahoo = **OPPORTUNITY**
- You're getting better value than half the industry thinks

#### GM Insights
```
Ja'Marr Chase
WR1 - Primary receiver, high-volume target
Workload: Entrenched WR1 - team's clear No. 1 target with elite target share
Offense: Joe Burrow-led passing attack; expected to lead the team in targets again
...
```
Each player card includes:
- **Workload security:** How locked-in is his role on the depth chart?
- **Offensive environment:** What's the quarterback/scheme situation around him?
- **Coaching/scheme impact:** Is a new coordinator or scheme changing his usage?
- **Contract outlook:** Extension, contract year, rookie deal, or free-agency risk — softened to avoid stale, overly specific claims
- **Injury/durability notes:** Current status plus any recurring durability concerns
- **Competition for touches/targets:** Who else on the roster is fighting for his volume?
- **Breakout/decline indicator:** Is his outlook trending up, stable, or risky?
- **Confidence/freshness tag:** Flags whether a note was manually verified against recent reporting or is a preliminary heuristic that should be double-checked before draft day

#### Risk Level
- 🟢 **Low** = Locked-in role, healthy, contract security
- 🟡 **Medium** = Injury history, role uncertainty, contract year
- 🔴 **High** = High bust risk, multiple concerns

*Why it matters:* A player's ADP might be great, but if his role, contract, or health situation looks shaky, that changes his value.

---

### Draft Log (Bottom Panel)
Running history of every pick:
- Organized by round
- Your picks highlighted in green
- Shows: Pick #, Player, Position, Team

*Why it matters:* Tracks league tendencies. "Team B always goes RB early"—now you know.

---

## 🎯 How to Use This for GM Strategy

### Example 1: Avoiding Reach Alerts
**Scenario:** You're on the clock, considering a player near ADP 2.08
- Dashboard shows tight consensus across FantasyPros, Yahoo, ESPN, and DraftKings
- Low variance = Market agrees, no shop alert
- **Decision:** If you need the position, this is fair value

### Example 2: Spotting Value
**Scenario:** A player appears in recommendations with a wide ADP spread across sources
- **ADP Variance** flagged as a Shop Alert!
- One source undervalues him relative to others
- **Decision:** Could be a steal depending on your league's bias

### Example 3: Positional Blocking
**Scenario:** Only a few elite RBs left, several teams still need RB
- **CRITICAL Scarcity Alert** appears
- You need WR, not RB, but...
- **Decision:** Grab the RB anyway or get blocked? This alert helps you decide.

### Example 4: Contract/Role Risk
**Scenario:** A player's GM insight card flags a contract-year situation and moderate competition for touches
- **Risk: Medium**
- **Decision:** Great talent, but the volume isn't guaranteed. Is that worth the pick this early?

---

## 📱 Mobile vs Desktop

### Phone/Tablet (Recommended)
- ✅ Easy to hold during draft
- ✅ Quick to tap "Log Pick"
- ✅ Can reference while watching broadcast
- ⚠️ Smaller screen = scroll more

### Laptop
- ✅ Bigger recommendations panel
- ✅ Easier to read GM insight notes
- ⚠️ Less portable
- ⚠️ Slower to input with 1-min clock

**Pro tip:** Use phone/tablet primary, have laptop as secondary reference.

---

## 🔧 How It Works (Technical)

### Files Explained

| File | Purpose |
|------|---------|
| `index.html` | Main dashboard (open this file) — the entire app in one static page, no backend |
| `data/players.json` | Player data, ADP rankings, GM insight notes |
| `README.md` | This file |

### Data Sources

**ADP (Average Draft Position):**
- FantasyPros - aggregates 100+ expert rankings
- Yahoo - your league's official platform
- ESPN - major sports media rankings
- DraftKings - sportsbook rankings (different scoring)

**GM Insights:**
- Workload security, offensive environment, and coaching/scheme impact: depth charts, coach/OC tendencies, and offensive context
- Contract outlook: publicly reported contract situations, softened to avoid stale or overly specific claims
- Injury/durability notes: current status plus recurring durability concerns
- Competition for touches/targets and breakout/decline indicator: how contested a player's role is and which direction his outlook is trending
- Confidence/freshness tag: whether a note is manually verified or a preliminary heuristic to re-check before draft day

### Scoring System
Dashboard is configured for your league:
- **Format:** PPR (0.5 points per reception)
- **Positions:** 1 QB, 2 RB, 2 WR, 1 TE, 1 FLEX, 1 K, 1 DEF, 7 bench, 1 IR
- **League ID:** 219725

---

## ⚠️ Important Notes

### This is NOT a Trade Simulator
- Doesn't predict who other teams will pick
- Doesn't optimize post-draft trades
- Use it for: Real-time draft decisions only

### Manual Input Required
- You log picks as they happen (quick clicks)
- No auto-sync with Yahoo Fantasy
- 1-minute clock = no time for fancy automation

---

## 🔄 Keeping data fresh

`data/players.json` includes a `metadata.last_updated` field and a `data_freshness_warning` note instead of a hard-coded date, because ADP and GM insight notes go stale quickly. Before you rely on this tool for a real draft:

- **Re-check ADP** against current FantasyPros/Yahoo/ESPN/DraftKings rankings — the numbers in this repo are a starting point, not live data.
- **Re-check GM insight notes**, especially any player whose `gm_insights.confidence` field says it's a preliminary/heuristic note rather than a manually verified one.
- **Watch for last-minute news:** injuries, suspensions, depth-chart changes, and trades can all invalidate a note within days of your draft.
- **Add players as needed:** edit `data/players.json` following the existing schema (each player needs `rank`, `name`, `position`, `nfl_team`, `adp`, `bye_week`, `injury_status`, `role`, `risk_level`, and a `gm_insights` object).

---

## 🎓 Learning Value (For Sports Management)

This tool teaches real GM decision-making:

1. **Market Inefficiency:** Why do different sources rank players differently?
2. **Risk Assessment:** Contract year? Injury history? Role security?
3. **Scheme Fit:** How does a new coach/OC change player value?
4. **Positional Scarcity:** When do you reach? When do you punt a position?
5. **Draft Strategy:** Reactive vs proactive—when do you deviate from plan?

Post-draft, you can analyze: "Did I predict scheme fits correctly?" "Were my risk assessments accurate?"

---

## 🐛 Troubleshooting

### "Data not loading"
- Make sure `data/players.json` is in the same folder as `index.html`
- Refresh your browser (Ctrl+R or Cmd+R)
- Check your internet connection

### "Player autocomplete not working"
- Data might still be loading (takes 2-3 seconds)
- Try typing the player's first name
- Manual entry works if autocomplete fails

### "Dashboard is slow"
- Close other browser tabs
- On mobile, close other apps
- Refresh the page

### "I need to add more players"
- Edit `data/players.json`
- Follow the format of existing players (see [Keeping data fresh](#-keeping-data-fresh))
- Refresh the dashboard

---

## 📞 Support

**Questions during draft?**
- Check the "How to Use" section above
- Look at the example scenarios

**Issues with the tool?**
- Check Troubleshooting section
- Make sure files are in the same folder

**Want to improve it?**
- This repo is the single, consolidated version of the tool — contribute directly here rather than maintaining a separate prototype

---

## 🏆 Good Luck!

Remember:
- **Speed matters:** Log picks fast, make decisions faster
- **Trust the data, but verify it:** Multi-source ADP + GM insights = an edge, as long as you've refreshed them recently
- **Stay flexible:** Scarcity alerts tell you when to pivot
- **Learn:** Review draft log post-draft to understand market tendencies

---

**League:** 219725 (10-team, PPR)
