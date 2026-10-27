# Research notes

Use this when collecting examples or when the user needs a reviewable recommendation. Adapt the format to the assignment; it is not a required document template.

| Field | Record |
|---|---|
| Surface and failure | A specific area and an observed problem |
| Evidence | URL or supplied artifact; inspection date; relevant state |
| Observation | What was visibly present or actually exercised |
| Mechanism | Why that behavior may address the target's problem |
| Uncertainty | What the available evidence cannot establish |
| Adaptation | How it would work with the target's content and components |
| Cost and verification | New requirements; checks that would confirm the result |

## Worked example: an empty import history

**Target:** A fictional team's import-history screen. Its empty view says "No imports" and exposes an unlabeled upload icon. A supplied screenshot confirms the first-time view; keyboard behavior is not known.

**Failure:** A first-time user cannot tell which file format is accepted or what a successful import will produce.

**Reference observation:** A supplied example from a different application labels its file control with accepted formats and shows a clearly marked sample result beneath it. The screenshot supports the content hierarchy, not claims about validation behavior.

**Mechanism:** Showing a labeled sample output beside the input teaches the format and outcome before the user commits a file.

**Adaptation:** Keep the target's existing upload component and icon pack. Add concise accepted-format text and a clearly labeled example row built from the target's own schema. Use invented sample values rather than real customer data. Do not copy the reference's artwork, colors, copy, or composition.

**Tradeoff:** Sample content can be mistaken for a completed import; make its label explicit and exclude it from real counts and actions.

**Verification:** Inspect the first-time view at desktop and mobile sizes. Confirm the sample cannot be selected as a real record, the upload remains keyboard operable, and actual history replaces the empty treatment after a successful test import. Run imports only in an authorized test environment.

This is a worked reasoning example, not a claim of research conducted against a real product.

## Choosing sources

Prefer a source that exposes the relevant behavior over a gallery thumbnail. Search for the surface plus its job: "upload empty state accepted formats", "search filters result counts", or "mobile table row details". For behavior, inspect the actual interface or documented interaction when available. For layout, a supplied screenshot may suffice if its limits are explicit.

Use the target's own previous versions when they provide relevant evidence. A design gallery is optional, not a dependency. A blocked source does not justify pretending it was inspected.
