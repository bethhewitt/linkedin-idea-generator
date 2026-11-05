# LinkedIn idea generator for Claude

A Claude skill that suggests 8 to 12 new LinkedIn post ideas for a business or person, and keeps a ledger of every idea it has suggested. Published, rejected and in-progress ideas don't come back as new, and neither do reworded versions of rejected ones.

It gives starting points only: a hook, an angle and a reason for each idea. It does not write finished posts.

## What it does each run

1. Sets up or reads the **ledger**: one table recording every idea and what happened to it (`raised`, `exploring`, `published`, `killed`).
2. Offers you a **review dashboard** if you don't have one yet, or pulls in the decisions you've made on it, plus your latest record of published posts.
3. Reads your source material: voice guide, offer, past posts, case studies, testimonials, saved ideas.
4. Suggests new ideas in three groups (new topics, new takes, from the archive), plus your in-progress and saved ideas.
5. Saves a dated menu and logs every idea in the ledger.

Then you decide, in chat (`explore 3`, `publish 5`, `kill 7`) or on the dashboard.

## Install (Claude Code)

```
/plugin marketplace add bethhewitt/linkedin-idea-generator
/plugin install idea-generator@linkedin-idea-generator
```

Then ask Claude for LinkedIn ideas, or "what should I post about?".

To update later:

```
/plugin marketplace update linkedin-idea-generator
```

### Without the plugin system

Copy `skills/idea-generator/` into `~/.claude/skills/` (for you, across all projects) or into `.claude/skills/` in a project.

## The dashboard

`skills/idea-generator/assets/dashboard.html` is a review page that runs as a claude.ai artifact. It shows one idea at a time with **Yes, explore it** / **No, kill it** / **Decide later** buttons (or the Y, N and L keys), asks for kill reasons, and lists what's being written, what's live and what's been killed. Decisions made there reach the ledger the next time the skill runs.

The skill offers to set it up for you the first time you run it in the Claude app (where artifacts are available). Say yes and it publishes the page privately to your claude.ai account and records its address in the ledger. Say "not now" and it asks again after 30 days; say you don't want one and it stops asking. You can also ask for it at any time.

**Branding:** the page ships in neutral greys. At setup, Claude takes your colours, font and logo from your brand guidelines, design files or website, checks they're readable, and shows you the result before publishing. To change it later, ask Claude to "restyle the idea dashboard"; your decisions are kept.

## Repository layout

```
.claude-plugin/
  plugin.json             plugin metadata
  marketplace.json        lets this repo be added as a marketplace
skills/idea-generator/
  SKILL.md                the skill
  assets/
    ledger-template.md    starting ledger, with a Setup block for where things live
    dashboard.html        review dashboard (offered on first run)
```

## Credits

Created by Beth Hewitt. Released under the [MIT licence](LICENSE).
