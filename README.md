# builder-persona

A Claude Code skill that helps builders — founders, operators, engineers, growth leads, anyone who makes things — build and maintain their personal brand across LinkedIn, Twitter/X, and XHS (Xiaohongshu).

**This is not an AI writing tool.** It doesn't generate generic content from keywords. It extracts content from your real building experience, calibrates it to your actual voice, and adapts it per platform — so every post sounds like you, not like ChatGPT.

---

## Why this exists

I spent 3 years building my personal brand across 4 platforms (Twitter, Jike, LinkedIn, XHS) — first as a founder building my own AI company, then as an operator running growth at a 10M-user AI startup.

Every platform has different rules. What works on LinkedIn (full paragraphs, professional narrative) dies on Twitter (too long) and falls flat on XHS (too cold, no story). I rewrote the same idea 3 different ways every time. Most AI writing tools made it worse — the output was generic, polished, and sounded nothing like me.

So I wrote down everything I learned — the voice calibration, the platform mechanics, the hook formulas, the anti-patterns, the algorithm knowledge — into a single skill file that teaches Claude how to do it right.

---

## What's inside

The skill has 7 modules:

### 1. Persona Definition
Not "what's your niche?" — that's a marketing question. Instead:
- What are you building right now?
- What do you see every day that outsiders don't?
- Where does your industry get it wrong?
- What changed your mind recently?

Produces a locked content angle using the formula:
> "While everyone focuses on X, I pay attention to Y because I see Z from building this."

### 2. Content Pillars (4 defaults)
- **Process > Outcome** — how you do things, not what you achieved
- **AI-Native Behavior** — how people using AI actually work differently (not tool reviews)
- **Building in Public (real)** — moments that genuinely shifted your thinking
- **Systems > Tactics** — underlying mechanics, not "5 growth hacks"

Rotation rules prevent repeating the same pillar or stretching one idea into 5 posts.

### 3. Voice Calibration
The biggest differentiator. Doesn't ask you to pick "professional / casual / funny." Instead:
- Extracts your voice from how you actually explain things
- Sets tone axes (emotional vs analytical, loud vs quiet, abstract vs concrete)
- Enforces hard red lines:
  - Never "In a world where AI..."
  - Never "Not X, but Y" constructions
  - Never "3 reasons why..." listicles
  - Never abstract inspiration without grounding
  - Never content about things you haven't experienced

### 4. Platform Playbooks

**LinkedIn** — paragraph-based, professional narrator, open with personal anecdote, close with open question. No broken-line poetry. No engagement bait.

**Twitter/X** — fragments, punchlines, retweet + one sharp comment. Includes the 6 ranking algorithm systems (GraphJet, SimClusters, TwHin, RealGraph, TweepCred, Trust & Safety), daily engagement routine, and content format priorities.

**XHS (Xiaohongshu)** — dual-title strategy (cover title for users: pain/pleasure/curiosity hook; body title for algorithm: topic + long-tail keyword). Broken-line rhythm. Chinese. Vulnerability OK. Story-first.

### 5. Hook Bank
6 proven hook patterns with examples + 10 anti-patterns that are banned.

**Works:**
- "I tried..." (first-person experiment)
- "When I first..." (beginner relatability)
- "Most tools / most people..." (soft contrarian)

**Banned:**
- "This will change everything..." (hype)
- "No one is talking about..." (dead cliche)
- "In a world where..." (cosmic opener)
- Any claim not backed by lived experience

### 6. Cross-Platform Repurposing
Same idea, different entry point. Never reuse hooks across platforms.

| Platform | Abstraction | Structure | Emotion |
|----------|------------|-----------|---------|
| LinkedIn | Idea-first, highest | Full paragraphs | Composed, thoughtful |
| Twitter/X | Punchline-first, lowest | Fragments | Detached, ironic |
| XHS | Story-first, mid | Broken lines | Vulnerable, honest |

Workflow: LinkedIn first (deepest) → compress to X → rewrite for XHS in Chinese.

Example — same core idea "skills are hard to verify in AI era":
- LinkedIn: "Resumes are becoming the new NFTs — they represent value that's increasingly hard to verify."
- X: "resumes are the new NFTs"
- XHS: "我付钱买过一个完全用不了的设计。简历写得天花乱坠，结果上手一天就知道，全是AI生成的。"

### 7. Behavioral Rules (meta-instructions for Claude)
- Sound like the builder thinking out loud, not a content agency
- Every post needs a concrete anchor (conversation, data point, product decision, surprise)
- CS + Psychology dual lens: "how will humans behave?" before "how does the system work?"
- Deepest emotional undercurrent: making contribution visible, quantifiable, not exploitable

---

## Who this is for

- **You're building something real** — startup, product, internal tool, team. You have hands-on work happening every day.
- **You have things to say but struggle to say them** — insights in your head that come out as generic mush when you try to write them down.
- **AI writing tools sound nothing like you** — you've tried ChatGPT/Jasper/etc and the output is too polished, too generic, too "content agency."
- **You post on multiple platforms** — and you're tired of manually rewriting the same idea 3 times.
- **Your title doesn't match your contribution** — you're not CEO but you're doing more than most founders. You want your work to be visible.

## Who this is NOT for

- **You don't do hands-on work.** This skill extracts content from real experience. No experience = no content.
- **You want to batch-produce "knowledge creator" content.** This skill deliberately slows you down — depth over volume.
- **You want to copy someone else's style.** The core logic is extracting YOUR voice, not templating someone else's.
- **You don't use Claude Code.** This is a `.skill` file that only runs inside Claude Code.

---

## Installation

### Option 1: Direct download
```bash
# Download the skill file
curl -O https://raw.githubusercontent.com/leave3644/builder-persona/main/builder-persona.skill

# Move to Claude Code skills directory
mv builder-persona.skill ~/.claude/skills/
```

### Option 2: Clone the repo
```bash
git clone https://github.com/leave3644/builder-persona.git
cp builder-persona/builder-persona.skill ~/.claude/skills/
```

That's it. No dependencies, no API keys, no config. Claude Code auto-discovers it.

---

## Usage

Open Claude Code and say any of these:

```
"Help me build my persona"
"Write a LinkedIn post about what I learned this week"
"I just shipped X — help me write about it for Twitter and XHS"
"Repurpose this LinkedIn post for Twitter and Xiaohongshu"
"What should I post about? Here's what I've been doing..."
```

The skill will guide you through persona definition (first time) and then generate platform-specific content calibrated to your voice.

---

## How it's different from AI writing tools

| | Generic AI writing | builder-persona |
|--|-------------------|-----------------|
| Starting point | "What topic do you want to write about?" | "What are you building? What surprised you recently?" |
| Voice | Pick a tone: professional / casual / funny | Extracted from how you actually talk and think |
| Output | One version, one platform | 3 versions, platform-native (LinkedIn / X / XHS) |
| Quality control | Grammar + fluency | Red lines: no listicles, no hype, no unearned claims |
| Algorithm awareness | None | X ranking systems, XHS dual-title strategy, LinkedIn engagement patterns |
| Language | English | English + Chinese (XHS) |
| Identity | Generic "founder" | Builder — anyone who makes things, regardless of title |

---

## License

MIT — use it, modify it, share it. If it helps you find your voice, that's the whole point.
