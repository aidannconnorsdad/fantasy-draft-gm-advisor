# ⚡ Fantasy Draft GM Advisor

**Real-time NFL fantasy football draft companion with multi-source ADP analysis, positional scarcity alerts, and GM intelligence.**

Built for serious fantasy managers who want data-driven draft decisions in a high-speed environment.

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
   - GM notes on role, scheme fit, contract status
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

#### GM Notes
```
Ja'Marr Chase
WR1 - Primary receiver, high-volume target
```
- **Role:** What's his job on the field?
- **Scheme Fit:** Does the new offense use him?
- **Contract Status:** Locked in or at risk?

#### Risk Level
- 🟢 **Low** = Locked-in role, healthy, contract security
- 🟡 **Medium** = Injury history, role uncertainty, contract year
- 🔴 **High** = High bust risk, multiple concerns

*Why it matters:* A player's ADP might be great, but if he's contract year (could be traded), that changes value.

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
**Scenario:** You're on the clock, considering Bijan Robinson (RB, ADP 2.08)
- Dashboard shows: "FP: 2.1, Yahoo: 2.0, Consensus: 2.08"
- Low variance = Market agrees, no shop alert
- **Decision:** If you need RB, this is fair value

### Example 2: Spotting Value
**Scenario:** Travis Etienne (RB) appears in recommendations
- Dashboard shows: "FP: 11.0, Yahoo: 9.5, Consensus: 10.2"
- **ADP Variance: 1.5** (Shop Alert!)
- Yahoo undervalues him, FantasyPros likes him
- **Decision:** Could be a steal depending on league bias

### Example 3: Positional Blocking
**Scenario:** Only 3 elite RBs left, 4 teams need RB
- **CRITICAL Scarcity Alert** appears
- You need WR, not RB, but...
- **Decision:** Grab the RB anyway or get blocked? This alert helps you decide.

### Example 4: Contract Year Risk
**Scenario:** Saquon Barkley (RB)
- Dashboard shows: "Contract year - could be trade candidate"
- ADP: 2.7 (very early)
- **Risk: Medium**
- **Decision:** Great player, but mid-season trade risk. Is that worth it?

---

## 📱 Mobile vs Desktop

### Phone/Tablet (Recommended)
- ✅ Easy to hold during draft
- ✅ Quick to tap "Log Pick"
- ✅ Can reference while watching broadcast
- ⚠️ Smaller screen = scroll more

### Laptop
- ✅ Bigger recommendations panel
- ✅ Easier to read GM notes
- ⚠️ Less portable
- ⚠️ Slower to input with 1-min clock

**Pro tip:** Use phone/tablet primary, have laptop as secondary reference.

---

## 🔧 How It Works (Technical)

### Files Explained

| File | Purpose |
|------|---------|
| `index.html` | Main dashboard (open this file) |
| `data/players.json` | Player data, ADP rankings, GM notes |
| `README.md` | This file |

### Data Sources

**ADP (Average Draft Position):**
- FantasyPros - aggregates 100+ expert rankings
- Yahoo - your league's official platform
- ESPN - major sports media rankings
- DraftKings - sportsbook rankings (different scoring)

**GM Intelligence:**
- Role/Scheme: Team depth charts, coach/OC tendencies
- Contract Status: Public contracts, extension eligibility
- Risk Level: Injury history, role uncertainty, age

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

### Data is Current as of Sept 2025
- ADP changes throughout preseason
- Consider updating player data mid-preseason if draft is late
- GM notes based on current team rosters (pre-draft)

### Manual Input Required
- You log picks as they happen (quick clicks)
- No auto-sync with Yahoo Fantasy
- 1-minute clock = no time for fancy automation

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
- Follow the format of existing players
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
- This is a starting point—Phase 2 coming post-draft
- After draft ends, we'll add deeper analysis

---

## 🏆 Good Luck!

Remember:
- **Speed matters:** Log picks fast, make decisions faster
- **Trust the data:** Multi-source ADP + GM notes = edge
- **Stay flexible:** Scarcity alerts tell you when to pivot
- **Learn:** Review draft log post-draft to understand market tendencies

Your son's got this. 💪

---

**Version:** 1.0  
**Last Updated:** Sept 1, 2025  
**League:** 219725 (10-team, PPR)
