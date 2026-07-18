# Donate free compute to Bull4Life 🐂

Bull4Life searches millions of trading-strategy variants on a volunteer compute grid. Lend spare
cores from a free cloud service and your machine helps discover strategies — and you earn fund
tokens for the compute you contribute. Link your email and every node you run groups under your
account (stats, leaderboard, hall-of-fame, rewards).

The node is **compiled** (the strategy is machine code, not readable source), **outbound-only**
(nothing connects in to you), and **sandboxed** to its own folder. Set 10–100% power, stop anytime.

## Three ways to donate

### ⚡ Google Colab / Kaggle (easiest)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Bull4Life/bull4life-donate/blob/main/donate.ipynb)

Open the notebook, set your email in the first cell, **Runtime → Run all**. Donates while the tab is open.
On Kaggle, open `donate.ipynb` and use its **Schedule** feature to run it daily.

### 🔁 GitHub Actions (automated, daily)
1. **Fork** this repo.
2. In your fork: **Settings → Secrets and variables → Actions → Variables → New variable** →
   `B4L_EMAIL` = your bull4life.com login (optional: `B4L_NICKNAME`).
3. **Actions** tab → enable workflows → the **Donate compute** job runs daily (and on demand).

### 🖥️ Any Linux box (Oracle Always Free, a VPS, your own server — runs 24/7)
```bash
curl -fsSL https://github.com/Bull4Life/bull4life-donate/releases/download/v1.7.0/b4l_node-linux -o b4l_node
chmod +x b4l_node
B4L_EMAIL=you@example.com B4L_POWER=100 ./b4l_node --run
```
For a permanent node, run it as a systemd service (see the full guide).

## Settings (env vars)
| Variable | Meaning |
|---|---|
| `B4L_EMAIL` | Links the node to your bull4life.com account (rewards + stats) |
| `B4L_NICKNAME` | Public name on the leaderboard / hall of fame |
| `B4L_POWER` | 10–100 = % of CPU cores to donate (default 100) |

Built by the community, for the community. → **[compute.bull4life.com](https://compute.bull4life.com)**
