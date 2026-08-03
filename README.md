### Builder-operator who ships production AI.

Ops roots, product instincts, both now aimed at AI. 4x founding hire. I built an A-Level AI tutor that the UK government selected for its national programme on safe AI tutoring. Allergic to GitHub? You can read more about what I'm building and writing here: [ElliotOS](https://www.elliotos.com/)

**Track record:** [Flash Pack](https://www.flashpack.com/) (pre-seed to Series A), [MealsForTheNHS](https://mealsforthenhs.org) (co-founder, £1.8m raised, 303k meals), [Farewill](https://farewill.com/) (SRA/FCA regulated).

**Background:** Languages BA (Birmingham/Fudan). French and English (native), Spanish (fluent), Chinese (intermediate). [BlueDot Impact](https://www.bluedot.org/) AI Governance and Alignment.

🎙️ **Podcast:** [Just Now Possible with Teresa Torres](https://open.spotify.com/episode/3D8quBCXrMNgIF87czhux3). Building AI products that augment human relationships rather than replace them.

---

### AI Tutor ([zerogravity.co.uk/tutor](https://www.zerogravity.co.uk/tutor))

An A-Level AI STEM tutor, in production across four subjects on every major UK exam board. Direct-to-consumer for individual students, with a school hub for teachers running it across their classes.

The UK government selected it for the [AI Tutoring Tools Pioneers Programme](https://www.gov.uk/government/news/edtech-and-ai-companies-invited-to-help-build-safe-ai-tutoring-tools-for-disadvantaged-pupils) (DfE and DSIT), a national cohort building safe AI tutoring for disadvantaged pupils, held to the government's Generative AI Product Safety Standards.

I built it on a multi-agent architecture. Coaching, practice, marking and assignments each ran as their own agent, with their own prompts, pedagogy and evaluator. It was Socratic from the prompt up, refusing to give the answer even when students got creative about asking. An always-on evaluator graded every coaching session against the Socratic spec, and safety telemetry ran on every interaction.

The hard part was never the AI. It was the operating system around it: correctness evaluation against real past papers and official mark schemes, and the discipline to ship every day while the safeguards only got tighter.

---

### AI builds

I build across the agent stack: MCP servers, Claude Code skills and hooks, multi-agent orchestration, evals, and autonomous loops. I use Claude Code daily on a production app, and most of these came from scratching my own itches.

| Project | What it does | Why it exists |
|---------|-------------|---------------|
| 💼 [boulot](https://github.com/ElliotJLT/boulot-os) | Open-source career-ops system that runs on your own laptop through Claude Code. Tailors your CV per role, then three adversarial agents (hiring manager, reviewer, strategist) fight over the draft. Company research, mock interviews, pipeline tracking | Built it for my own search in a brutal market. It worked, so I open-sourced it. Agent-native by design — markdown persona, code tools, your data stays on your machine |
| 🛡️ [ward](https://github.com/ElliotJLT/ward) | Safeguarding safety layer for LLM apps that serve under-18s — screens each message, splits ordinary conduct from a genuine disclosure, routes real disclosures to a human on a clock. Grounded in UK statute (KCSIE 2025) | Most AI reaching kids has no safeguarding process. A Claude-as-judge detector hits 90% recall, 100% precision and 0% false-positives on the eval that ships inside it, and a deterministic response guard checks the reply back to the child is safe too |
| 📋 [homebuyer-mcp](https://github.com/ElliotJLT/homebuyer-mcp) | UK home-buying MCP server — conveyancers and mortgage brokers from SRA/FCA/Companies House registers, stamp duty, lease checks, survey explainer, title register analysis | Buying a house means chasing conveyancers, brokers and registers across half a dozen sites. This is the whole journey in one server: 11 tools, live regulatory data cross-referenced with company health |
| 🎙️ [vox](https://github.com/ElliotJLT/vox) | Voice of Customer research agent | VoC research is weeks of reading call transcripts before a pattern shows. Vox does 8 days of it in 8 minutes: JTBD, personas, opportunity mapping from Gong/Granola/Jiminy data |

### Agent & Claude Code tooling

| Project | What it does | Why it exists |
|---------|-------------|---------------|
| 🎨 [dabble](https://github.com/ElliotJLT/dabble) | Visual editor for server-rendered (Hotwire) apps — edit the running app in place, write real ERB, built for AI coding agents | Design tools generate React and ignore server-rendered stacks. Dabble edits the running Hotwire app in place: click an element → tweak it → your agent gets the exact source and selection context. No design→code handoff |
| 🧪 [My-Claude-Skills](https://github.com/ElliotJLT/Claude-Skill-Potions) | Curated Claude Code skills for ops and product workflows | The skills directory is 40K+ deep. These are the ones that actually work |
| 🍋 [zeste](https://github.com/ElliotJLT/zeste) | macOS menubar app — search, install, and manage Claude Code skills | Finding and installing skills shouldn't require digging through GitHub |
| 🪝 [hooksmith](https://github.com/ElliotJLT/hooksmith) | Browse and install pre-built Claude Code hooks with one command | CC hooks are powerful but there's no easy way to find and install them. The missing package manager: 12 hooks, one command, zero config |
| 🔍 [claudemd-lint](https://github.com/ElliotJLT/claudemd-lint) | Linter for CLAUDE.md files | CLAUDE.md files rot into vague rules and bloat that quietly degrade the agent. This lints them: catches vague rules, bloated configs, and instructions that should be hooks |

### AI behavior research

Controlled experiments on how Claude actually behaves, not how it's assumed to.

| Project | What it found |
|---------|---------------|
| 🧠 [crux](https://github.com/ElliotJLT/crux) | Capture human decisions during AI-assisted development | When an agent writes the code, the reasoning behind each human call vanishes from the diff. Crux records which calls were made and why, so you can audit and learn from them later |
| 🐕 [dog-years](https://github.com/ElliotJLT/dog-years) | Claude quotes human-team timelines ("2-3 weeks") for work it does itself in minutes. The real question is whether that bad estimate changes what it actually does. A fix that grounds future estimates in measured history instead of vibes |
| 🧭 [agent-orchestration-research](https://github.com/ElliotJLT/agent-orchestration-research) | Research notes on multi-agent coding workflow patterns and orchestration strategies |

### Fun stuff

| Project | What it does |
|---------|-------------|
| 墨 [mo-hanzi](https://github.com/ElliotJLT/mo-hanzi) | Menubar SRS for learning Chinese characters (HSK 1-3) |
| 💡 [lamplight](https://github.com/ElliotJLT/lamplight) | An open street-lighting map for running after dark |
| 🎧 [spotifyunwrapped](https://github.com/ElliotJLT/spotifyunwrapped) | Your Spotify data, visualised properly. Privacy-first analytics, runs entirely in your browser |

### What I'm writing

- [What I Learned Spending A Week With 100+ AI Leaders](https://medium.com/@elliotJL/what-i-learned-spending-a-week-with-100-ai-leaders-3517ac3dc16c)
- [What I Learned Shipping AI to Users Who Can't Afford Bad Advice](https://medium.com/@elliotJL/what-i-learned-shipping-ai-to-users-who-cant-afford-bad-advice-606243049534)
- [Amsterdam Built the 'Perfect' Ethical AI System. It Still Failed.](https://medium.com/@elliotJL/amsterdam-built-the-perfect-ethical-ai-system-it-still-failed-here-s-why-8dc8072beea3)
- [The Trust Gap: Why Your AI Product Will Fail Without This](https://medium.com/@elliotJL/the-trust-gap-why-your-ai-product-will-fail-without-this-92b8f60391b3)
- [Claude Keeps Making the Same Mistakes. So I Started Writing Down the Fixes.](https://medium.com/@elliotJL/your-ai-has-infinite-knowledge-and-zero-habits-heres-the-fix-e279215d478d)

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-hireelliot-blue?logo=linkedin)](https://www.linkedin.com/in/hireelliot/) [![BlueDot Impact](https://img.shields.io/badge/BlueDot_Impact-AI_Governance_&_Alignment-4A90D9)](https://www.bluedot.org/)
