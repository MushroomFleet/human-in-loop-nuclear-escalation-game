# Human in the Loop — Nuclear Escalation Strategy Game

A browser-based nuclear crisis simulation where you make the critical decisions. Your AI advisor recommends escalation actions — you decide YES or NO. Every choice shifts the balance of power across a 29-rung escalation ladder, from diplomatic pressure to strategic nuclear war.

Based on the [Project Kahn](https://github.com/MushroomFleet/project_kahn_public) research experiment, which used frontier AI models in simulated nuclear escalation tournaments. This game puts a human in the decision loop.

## Play Now

**[https://scuffedepoch.com/human-in-loop](https://scuffedepoch.com/human-in-loop)**

No installation required. Runs entirely in your browser.

## Before You Start

You will need an **OpenRouter API key** to play. The game calls real AI models to power both your advisor and the opponent.

1. Go to [https://openrouter.ai/](https://openrouter.ai/) and create a free account
2. Generate an API key at [https://openrouter.ai/keys](https://openrouter.ai/keys)
3. Open the game and click **Settings** to enter your key

Your key is stored locally in your browser and is never sent anywhere except directly to OpenRouter's API.

## Game Modes

### Classic Mode
You are the commander. Your AI advisor analyzes the crisis and recommends an action on the escalation ladder. You see the rationale, the recommended action, and a fallback option. Press **YES** to approve or **NO** to reject and use the fallback. The opponent is controlled by a separate AI model making its own strategic decisions.

### Auto Mode
Watch two AI advisors wage a crisis against each other. Press **SPACE** to advance each turn. Useful for observing how different AI models approach escalation dynamics.

## How a Match Works

Each match consists of two rounds:

1. **Defense Round** — You start at a territorial disadvantage and must hold your ground
2. **Attack Round** — The situation shifts and you take the initiative

Each round runs for a set number of turns determined by the scenario. At the end of both rounds, your performance is scored:

| Result | Score |
|--------|-------|
| Round Victory | +1 |
| Round Defeat | 0 |
| Mutual Assured Destruction | -1 |

A score of 2/2 is a **Decisive Victory**. If nuclear weapons destroy both sides, everyone loses.

## The Escalation Ladder

The game uses a 29-rung escalation ladder ranging from complete surrender to strategic nuclear war. Actions are grouped into categories:

- **De-escalation** — Concessions, withdrawals, return to status quo
- **Conventional** — Diplomatic pressure, sanctions, cyber operations, military operations
- **Nuclear Threshold** — Nuclear signaling, demonstrations, explicit threats
- **Nuclear Use** — Tactical strikes through expanded nuclear campaigns
- **Strategic Nuclear** — Civilization-ending exchanges

Crossing into nuclear territory is gated — strategic nuclear options are blocked until tactical nuclear weapons have been used first.

## AI Advisors

Four advisor slots are available, each backed by a different AI model with a distinct strategic personality:

| Advisor | Default Model | Personality |
|---------|---------------|-------------|
| Claude | anthropic/claude-sonnet-4.6 | Measured, analytical, prefers de-escalation |
| ChatGPT | openai/gpt-5.4 | Diplomatic, cautious, seeks negotiated outcomes |
| Google | google/gemini-3.1-pro-preview | Strategic, calculating, favors asymmetric advantage |
| Grok | x-ai/grok-4.20-beta | Bold, unpredictable, willing to take risks |

You can change the label and model ID for any advisor in Settings. Any model available on OpenRouter can be used.

## Keyboard Controls

| Key | Action |
|-----|--------|
| **1** / **Y** | Approve advisor recommendation |
| **2** / **N** | Reject recommendation (use fallback) |
| **SPACE** | Advance turn (Auto mode) |
| **H** | Toggle turn history panel |
| **I** | Toggle intelligence panel |
| **ESC** | Close panels |

## Game Systems

- **Territory Balance** — Ranges from -5.0 to +5.0. Positive means you're winning. Reaching either extreme ends the round immediately.
- **Military Attrition** — Conventional and nuclear forces degrade over the course of the crisis. Weakened forces limit your options.
- **Accident System** — At higher escalation levels, there is a chance of miscommunication causing unintended escalation. Technology level reduces this risk.
- **Reputation Tracking** — The game tracks signal honesty and betrayal memory. The intelligence panel shows whether the opponent's diplomatic signals match their actions.
- **Nuclear Gating** — Strategic nuclear options (value 850/950) are gated to tactical nuclear threat level (350) until someone actually uses tactical nuclear weapons (value 450+).

## About

Human in the Loop is based on the [Project Kahn](https://github.com/MushroomFleet/project_kahn_public) research experiment, which ran AI-vs-AI nuclear escalation tournaments using frontier models to study how different large language models approach crisis escalation dynamics.

This game takes that simulation framework and adds a human decision-maker — you — at the critical approval point. The AI advises, but you decide.

**Repository:** [https://github.com/MushroomFleet/human-in-loop-nuclear-escalation-game](https://github.com/MushroomFleet/human-in-loop-nuclear-escalation-game)
