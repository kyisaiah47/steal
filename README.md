# Steal

A design precedent research skill for **Codex and Claude Code**. Find the mechanism behind a useful reference, adapt it to your own interface, and verify the result.

Use it when a screen feels generic but you need a concrete diagnosis, when researching a specific interaction, or when a reference looks promising and you want to understand which part is worth adapting. It supports research-only work as well as authorized implementation.

## Example

> The import-history screen feels unhelpful on first use. Use Steal to find relevant empty-state examples, explain what helps, and improve this screen using our existing components. Preserve the upload flow and the rest of the page.

The workflow identifies the actual failure, inspects relevant evidence, selects a focused mechanism, and checks the changed screen. It does not copy a reference's branding, assets, or proprietary code. See the [worked example](skills/steal/references/research-notes.md).

## Install in Codex

Copy the skill into a project's `.agents/skills/` directory, or your personal `~/.agents/skills/` directory. The following project install refuses to overwrite an existing skill:

```sh
git clone https://github.com/kyisaiah47/steal.git
cd /path/to/your-project
mkdir -p .agents/skills
test ! -e .agents/skills/steal && cp -R /path/to/steal/skills/steal .agents/skills/steal
```

Start a new Codex conversation. Invoke `$steal`, or describe a matching task. The repository also includes a portable plugin manifest for plugin-directory distribution; directory approval and availability are separate from installing the files.

## Install in Claude Code

From a Claude Code session:

```text
/plugin marketplace add kyisaiah47/steal
/plugin install steal@steal
```

Start a new session, then invoke `/steal:steal` with your target and desired scope. Alternatively, copy `skills/steal/` into your project's `.claude/skills/` directory without overwriting an existing folder, then invoke `/steal`.

For a temporary preview without installing:

```sh
claude --plugin-dir /path/to/steal
```

## Useful requests

- **Research only:** "Use Steal to research clearer search filters for this screen. Do not edit files."
- **Scoped improvement:** "Use Steal to improve the empty state in this route. Keep our layout, icons, and upload behavior."
- **Study a reference:** "Explain the mechanism in these supplied examples and whether it fits our mobile results table."

## Requirements and limits

The skill contains instructions and a worked example, with no runtime scripts, MCP server, account requirement, or API key. Real reference research needs an available browser/search capability or supplied evidence. The host's normal tool permissions still apply.

The skill cannot make unavailable browsing tools appear, inspect gated content without access, or prove interactive behavior from a screenshot. It reports evidence gaps. It does not authorize purchases, external publication, deployment, or broader redesigns. Browser captures and testing artifacts follow your environment's retention rules.

Both platforms load the same core instructions. Platform-specific private tooling and house design rules are intentionally absent.

## Validation

Run the skill-creator metadata validator against `skills/steal`, and run `claude plugin validate . --strict` to check the Claude package. Behavioral evaluation prompts and acceptance criteria are in [evals/scenarios.md](evals/scenarios.md). These scenarios check evidence handling, scope, and adaptation; passing package validation alone does not demonstrate design quality.

## Rights

Copyright 2026 Compound Labs. All rights reserved. See [LICENSE](LICENSE) for permission to install and use the package. Research references and users' project assets retain their own rights.

## Privacy and terms

Read the [data-handling policy](PRIVACY.md) and [usage terms](LICENSE) before use.
