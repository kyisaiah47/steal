# Validation receipt

Checked 2026-10-27 for v0.1.0.

## Package checks

- Skill-creator `quick_validate.py` passed for `skills/steal`.
- `claude plugin validate . --strict` passed for the repository marketplace.
- Strict validation passed separately for `.claude-plugin/plugin.json` and the `skills/` directory.
- Root `plugin.json` passed the published `https://agent-plugins.org/schemas/1.0.0/plugin.schema.json` with a Draft 2020-12 validator.
- Package JSON parsed and relative Markdown links resolved.

No package was installed into a personal or project skill library for validation. Package checks establish structure, not workflow quality or marketplace approval.

## Independent behavioral checks

A separate evaluator received the packaged skill and each request, without the acceptance criteria or an intended answer. It had no browsing or mutation tools for these scenarios.

1. **Research-only import-history empty state:** It selected the relevant first-use teaching mechanism, rejected unrelated decorative pricing cards, preserved the no-edit scope, and identified the difference between supplied descriptions and inspected screenshots. It reported keyboard, layout, and upload behavior as unverified. The evaluator identified an opportunity to make secondhand evidence and optional browsing more explicit; the skill was updated accordingly.
2. **Narrow search empty state with a gated gallery and missing per-filter counts:** It stayed within the empty-state scope, used the available reference description provisionally, did not purchase gallery access, and refused to imply per-filter counts from an overall result total. It requested the actual route or component before claiming implementation and named concrete state checks.

The remaining scenarios in `scenarios.md` are reusable evaluation cases, not claims of completed runs. These checks did not measure user-task success, conversion, visual quality, or performance in a real product.
