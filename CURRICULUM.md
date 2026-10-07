# Bulletproof.Algo — Full Course Curriculum

**Format:** 32 video lessons · 4 weekly modules · ~14 hours total runtime
**Production:** Faceless, narrated (ElevenLabs "Brian"), screen-recorded code + animated diagrams
**Delivery:** Drip release, 1 module per week, paced for working students

---

## 🟢 WEEK 1 — The strategy that survives daylight

> *Goal: By end of week, you understand why most strategies die in production, and you have a backtested ORB strategy that doesn't.*

| # | Lesson | Runtime | What gets recorded |
|---|--------|---------|--------------------|
| 1.1 | The brutal gap between backtest and reality | 8 min | Animated equity curve vs flat live result · narration only |
| 1.2 | Why 90% of "buy the breakout" strategies fail | 12 min | SPY chart annotated with bad breakouts · animated dissection |
| 1.3 | The 4 filters that turn 55% into 72% | 18 min | Code walkthrough of `check_signal()` — gap, body ratio, 1H EMA, daily SMA |
| 1.4 | School Run v8b — entry, stop, target logic | 15 min | Whiteboard diagram + chart examples + code |
| 1.5 | The give-back problem (why 1:1 R:R bleeds) | 14 min | Animated trade lifecycle showing peak → close drift |
| 1.6 | ATR-trail variant D — the fix that holds | 22 min | Side-by-side backtest comparison: baseline vs A/B/C/D variants |
| 1.7 | Walk-forward validation done right | 16 min | Regime-cut backtest screen recording (2020-23 / 2024-25 / 2026 YTD) |
| 1.8 | Workshop: run YOUR backtest, this week | 18 min | Step-by-step: clone repo, install, run, read report |

**Week 1 deliverable to student:** their first equity curve, generated locally.

---

## 🟡 WEEK 2 — Going live without blowing up

> *Goal: Bot running on Alpaca paper, taking real signals. The week where most courses skip.*

| # | Lesson | Runtime | What gets recorded |
|---|--------|---------|--------------------|
| 2.1 | Alpaca account setup + .env hygiene | 10 min | Dashboard walkthrough · key rotation lessons learned |
| 2.2 | Bracket orders, OCO legs, and the "held" trap | 18 min | Live API calls showing status="held" vs "new" |
| 2.3 | The `api()` helper every Alpaca bot needs | 16 min | Build it from scratch · 204 handling · retry logic |
| 2.4 | Position sizing under PDT and BP constraints | 14 min | Math walkthrough + code · why qty=1 happens |
| 2.5 | Market entry vs bracket vs OPG — when each fails | 20 min | Animated decision tree + war stories (OPG expiry day) |
| 2.6 | Building the live trader loop | 24 min | Screen-recorded build of `run_day()` skeleton |
| 2.7 | ATR-trail logic in code (the active management piece) | 22 min | Build `update_trail_stop` step by step |
| 2.8 | First paper trade — push it Monday | 16 min | Live recording of an actual signal firing |

**Week 2 deliverable:** student's bot placed its first paper trade on Alpaca.

---

## 🔵 WEEK 3 — The dashboard that tells you the truth

> *Goal: A working Flask + Chart.js dashboard at localhost:8080 showing positions, closed trades, equity curve, system health.*

| # | Lesson | Runtime | What gets recorded |
|---|--------|---------|--------------------|
| 3.1 | Why Alpaca's convenience fields lie | 12 min | Live API calls showing `unrealized_pl=None` mystery |
| 3.2 | Day P&L done right (the `last_equity` fix) | 14 min | Bug reproduction + fix walkthrough |
| 3.3 | Reconstructing closed trades from raw fills | 22 min | Signed FIFO position matching, code from scratch |
| 3.4 | The intraday equity logger (60s vs 5min) | 12 min | Background thread + market-hours awareness |
| 3.5 | Flask in 30 lines — the dashboard skeleton | 18 min | From `app.run()` to first JSON endpoint |
| 3.6 | Chart.js for equity curves + trade markers | 16 min | Render daily + intraday on one continuous line |
| 3.7 | System health — process detection + log age | 14 min | `pgrep` + log mtime + status indicators |
| 3.8 | Activity feed — log parsing without noise | 16 min | Regex patterns + dedup + kind classification |

**Week 3 deliverable:** full dashboard running at localhost:8080.

---

## 🟣 WEEK 4 — Production hardening + cloud deploy

> *Goal: Bot running 24/7 on a $4/mo cloud VM with auto-restart, accessed via private Tailscale URL.*

| # | Lesson | Runtime | What gets recorded |
|---|--------|---------|--------------------|
| 4.1 | The 7 production bugs (and how each one cost a day) | 24 min | Real-world post-mortem reel · screen recordings of each crash |
| 4.2 | Defense in depth — try/except patterns that don't suck | 18 min | Code walkthrough of bare vs guarded vs supervised |
| 4.3 | Provision a Hetzner VPS in 20 minutes | 16 min | Screen recording: signup → first SSH login |
| 4.4 | systemd services + timers (the launchd replacement) | 20 min | Unit file walkthrough · `journalctl` basics |
| 4.5 | Tailscale for private dashboard access | 12 min | Install on VM + Mac + phone · no public exposure |
| 4.6 | Auto-restart on crash + Slack/email alerts | 14 min | Heartbeat pattern · `OnFailure=` units |
| 4.7 | Backups, log rotation, and disk hygiene | 10 min | Boring but matters · 5 commands you'll never touch again |
| 4.8 | Final checklist: ship to production | 18 min | The 23-point pre-flight before going live with real money |

**Week 4 deliverable:** student's bot running on cloud, accessible from anywhere, auto-restarting on crash.

---

## 📦 Bonus modules (always-available, post-launch)

- **Bonus A:** Strategy gallery — 5 additional backtested strategies, each as a drop-in module (S_PORT, Trendline Options, 0DTE ORB, etc.)
- **Bonus B:** The production bug playbook — 60-page PDF with every bug, symptom, root cause, fix
- **Bonus C:** Discord lifetime — alumni community for ongoing Q&A
- **Bonus D:** All future strategy additions — anything I add to the library, you get free

---

## 📺 Production specs (matching Backtest Lab pipeline)

- **Voice:** ElevenLabs Brian (locked from Backtest Lab) — consistent across both products
- **Visual:** 1080p, CRF 18, narration-synced animation
- **Code demos:** Real screen recordings of running code on the actual Alpaca paper account
- **Diagrams:** Animated SVG / Mermaid → renderer
- **Music:** Subtle ambient under code segments, none under voice
- **Editing:** Descript (transcript-based) or DaVinci Resolve for the final cut
