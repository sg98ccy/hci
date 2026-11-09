# HCI

Help people understand an interface, use it comfortably, and recover when something goes wrong.

This agent skill brings human-computer interaction (HCI) guidance into design, implementation, and review. It helps you choose useful improvements for the people using your product, with sources behind the recommendations.

## When to use it

- Make navigation, controls, and information easier to understand.
- Design loading, error, cancellation, and recovery states.
- Help people inspect and correct AI suggestions.
- Review interactions in websites, apps, maps, dashboards, or XR.
- Plan or assess a usability study around representative tasks.

The skill works with your existing design language and project constraints. It applies relevant concepts, such as clear feedback or grouping related controls, rather than requiring a particular visual style or a full redesign.

## Use with your AI agent

This skill uses the open [Agent Skills format](https://agentskills.io/home): Markdown instructions with supporting files. **The skill itself requires no Node.js or npx.** Use it with an agent that supports skills, or provide the instructions directly to an agent that can read them.

### Manual setup

1. [Download this repository as a ZIP](https://github.com/sg98ccy/hci/archive/refs/heads/main.zip) and extract it, or clone the repository.
2. Copy `SKILL.md` with its supporting files and folders into a folder named `hci` in your agent's skills directory. Keep the relative file structure intact.
3. Open your project with the agent and try a prompt below.

Common project-level locations are:

| Agent | Skill folder in your project |
| --- | --- |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/hci/` |
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/hci/` |
| [GitHub Copilot](https://docs.github.com/en/copilot/concepts/customizations/agent-skills) | `.github/skills/hci/` |
| [OpenCode](https://opencode.ai/docs/skills/) | `.opencode/skills/hci/` |
| [Codex](https://learn.chatgpt.com/docs/build-skills) | `.agents/skills/hci/` |

Follow your agent's linked documentation for other locations or hosted setups. For an agent without native skill discovery, attach or provide [SKILL.md](SKILL.md) and any supporting files it needs, then explicitly ask it to apply the guidance.

<details>
<summary>Optional: install with the Skills CLI</summary>

The [Skills CLI](https://github.com/vercel-labs/skills) can copy the skill into supported agents' directories. **This optional installation method requires Node.js with npx** and network access.

Run from your target project and use the installer to select your agent:

```sh
npx --yes skills@latest add https://github.com/sg98ccy/hci --skill hci
```

On Windows PowerShell, use `npx.cmd` if your execution policy blocks `npx`.

</details>

## Try it

Give your agent the relevant screen, code, or task context:

```text
Use the hci skill to review this settings screen. Make the most common
action easy to find and help users recover from errors. Keep the current
visual style.
```

For a more focused interaction:

```text
Use the hci skill to design the progress, cancellation, and retry states for
this file-upload flow. Explain the main tradeoffs.
```

Discovery and invocation depend on your agent. Use its skill selector or mention syntax when available. For example, Codex supports `$hci` ([guide](https://learn.chatgpt.com/docs/build-skills)); the prompts above use plain language so you can adapt them to your agent.

## What to expect

The agent focuses on the concepts useful to your task, explains consequential choices, and checks the relevant interaction states. It distinguishes design judgement and automated checks from evidence gathered with actual users. A review can identify likely problems; usability and accessibility claims still need appropriate evaluation.

Read [SKILL.md](SKILL.md) for the full guidance, concept references, and original sources. [agents/openai.yaml](agents/openai.yaml) contains optional invocation metadata for OpenAI tools.

## Update or customize

Edit [SKILL.md](SKILL.md) in your source checkout. Refresh a manual installation by copying the updated skill files into your agent's skill folder. If you used the optional CLI, rerun its install command to refresh from GitHub, or replace the GitHub URL with your local checkout's path. Quote paths containing spaces.

Installed copies do not automatically sync with a source checkout. Keep your changes in the source you maintain, then refresh the copies you use.

For an existing personal `devsetup` installation, `devsetup skills-core` is an optional shortcut that installs the core bundle for Codex from configured local sources.

## Related skills

- [Clear Writing](https://github.com/sg98ccy/clear-writing): help readers understand explanations, instructions, and interface text.
- [Coding Practices](https://github.com/sg98ccy/coding-practices): make implementation boundaries, ownership, and reuse easier to reason about.
