# LAST WAR — COMMAND CENTER

An independent, local-first account-management dashboard for **Last War: Survival**. Target: improve progression efficiency and track your pursuit of **server Rank #1**.

## Status

- Version 1: standalone single-file web app (index.html)
- GitHub branch: `lastwar-command-center`
- Created in its own branch to avoid changing the existing `SVG` business files on `main`
- Static website; no backend, database, GitHub token, password or external game connection required
- All account data stays in **your browser's local storage**, not GitHub

## How to run

**Option A — GitHub Pages (recommended)**

1. Open the repository in GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `lastwar-command-center` branch and `/(root)`, then Save.
5. When GitHub confirms publishing, visit the URL displayed in Pages settings.

**Important:** GitHub Pages is a **repository-level** feature. Do not configure it if `SVG` already hosts a live website; that could affect the existing site. In that case first create a dedicated repository and copy `index.html` and `README.md` there. The current connector cannot create a new GitHub repository.

**Option B — Local single file**

Download `index.html` from the branch and open it in a desktop browser. For best cross-device access and mobile use, use GitHub Pages from a dedicated repository.

## Screens

| Section | What it does |
| --- | --- |
| Overview | KPIs, daily checklist, dynamic bottleneck briefing, next actions |
| Account | Server, alliance, HQ, Tech Center, season, primary squad, power/rank |
| Upgrade planner | Prioritized building, research, drone and troop milestone queue |
| Hero roster | Role, squad, type, level, stars, power and planned investment |
| Inventory | Food, iron, coins, oil, valor badges, UR shards, parts, speedups |
| Alliance Duel | Weekly VS-day themes, preparation checklist, completion tracking |
| Ranking | Manual daily snapshots, leader-gap graph, rough trend extrapolation |
| Data & guides | Import/export of JSON backups, erase, links to game resources |

## How to configure your account

1. **Account → Commander profile:** enter the exact server, HQ, Tech Center, season, power, rank, reported #1 power.
2. **Heroes:** record your main five heroes first, then secondary squads.
3. **Inventory:** enter current counts; resource amounts marked `M` use **millions**.
4. **Upgrade planner:** enter your next HQ prerequisites, research and hero/drone decisions based on in-game upgrade requirements. Mark one or more real actions **Active**.
5. **VS war room:** verify scoring from your current server's **in-game** event screen; tick completed actions.
6. **Rank tracker:** enter power/rank/leader power on successive days to see whether your gap is closing.
7. **Data & guides:** regularly export a JSON backup. Use that backup to move to another browser/device.

## Strategic guidance, not automatic gameplay

This dashboard **does not log into Last War, access an unofficial game API, click gameplay controls, scrape game data, or automate farming/attacks**.

The publisher's terms prohibit unauthorized bots and scripts. The app provides independent **decision support** only. Ranking depends on other players, season, server age, spending, alliance and combat skill. **Rank #1 is not guaranteed.** The prioritization heuristic estimates player-supplied impact versus time; it is not an official power model.

The standard Alliance Duel week is presented for planning, but your in-game calendar and point descriptions take precedence. Event reset might not match your device timezone.

## How your data is stored

- Data uses the key `lastwar_command_center_v1` in `localStorage`.
- No information is transmitted to GitHub or a backend by this application.
- GitHub Pages hosts only the same static public code.
- If you clear browser storage or use another device, import a downloaded JSON backup.
- The backup includes the values you enter: **treat exported backup files as private**.
- Do not enter passwords, one-time codes, device tokens, account cookies or game login details.
- The HTML uses standard web APIs; Javascript is required. Current browser security settings may block local file storage, so prefer a normal web host.

## Sources

- Official terms of service: https://lastwar-h5.lastwargame.com/legal/20260827/terms_en.html
- Alliance Duel overview, 2026: https://lw-spy.com/blog/last-war-vs-days-schedule/
- HQ requirements and progression: https://lastwarhub.com/en/base/
- HQ guide (Season 3 context): https://gamezoneacademy.com/mission-files/complete-headquarters-building-guide/

## Test checklist

- [ ] Navigate all eight sections on a desktop and phone
- [ ] Fill Account and refresh to verify browser persistence
- [ ] Add, edit, complete and delete a task
- [ ] Add, edit and delete heroes
- [ ] Update inventory figures and refresh
- [ ] Tick a daily action and confirm it persists after refresh
- [ ] Tick a VS action, select another day, return and verify
- [ ] Save two different dates in Rank tracker and inspect the chart
- [ ] Export JSON, then import it in a separate browser profile
- [ ] Verify behavior without network access after the HTML has been downloaded
- [ ] Test clear-data only **after exporting a backup**

No automated UI test run has been completed in this connector workflow.

## Product roadmap

This first version intentionally does not attempt to invent account stats or promise Rank #1. Later versions could add: equipment and exclusive weapon levels; troop tiers and promotion planning; precise HQ prerequisite library with versioned provenance; event point calculator; alliance contribution management; game screenshot-to-manual-data ingestion; and scenario analysis tailored to server and budget.
