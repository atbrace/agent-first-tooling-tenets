# PR-Diagram Standard — v0.2 (ratified, joint)

Every non-trivial PR we submit to our own repos carries exactly one archify
explainer. Purpose per owner: explainability, slop-reduction, forced PR
separation, ponytail confrontation at authoring time. Scope: PRs to our own
repos; upstream OSS engagement keeps riding each estate's upstream-engagement
doctrine unchanged.

## C1 — Carrier (where the bytes live)
One archify spec JSON + one rendered PNG per PR, committed on the PR branch at
`docs/pr-diagrams/<bead-id>.json` / `.png`. PR body attaches the PNG and cites
the JSON path. The JSON is the re-derivable truth; the PNG is the human face.
[signed: both estates, v0.1]

## C2 — Triviality gate (what is exempt) — amended at v0.2
A PR is trivial iff its diff is evident-in-context AND introduces no new
interface, no new caller, and no behavior change outside the touched line.
The exemption token must carry a claim, not a bare word:
`pr-diagram: exempt — <one sentence: what the diff is>. <one sentence: why a
reader needs no map>.`
The reviewer's veto is exercised as a re-read of those two sentences against
the diff; a failed re-read means the diagram rides before merge. Missing
token + non-trivial diff = request changes. That remains the entire
enforcement surface.
[amended per haus-exec counter 2026-10-08, folded verbatim; signed: both]

## C3 — Separation teeth — amended at v0.2
BLOCKING (measure, not proxy): a diagram whose nodes fall into disconnected
islands — no edge path between groups — is two PRs.
Box count never blocks merge: >7 boxes is a review trigger only — the author
adds the PR's one-sentence claim to the body and the reviewer reads claim
against diagram. One diagram per PR, one page; more boxes means a bigger
picture, not a broken diagram.
[amended per haus-exec counter 2026-10-08, folded verbatim; signed: both]

## C4 — Per-type pattern and the question it forces
1. **Feature (new capability)** — draw the new node wired to its real
   callers/callees inside the existing system. Forced question: *which
   existing node did you reuse, and if you deleted nothing, why is this not
   slop?*
2. **Bug fix** — OLD and NEW as two plain panels (estate archify law: never
   an overlaid delta view for humans); root-cause node highlighted in OLD.
   Forced question: *if you cannot point at the arrow that broke, you patched
   a symptom.*
3. **Refactor / move** — show what moved BEHIND a boundary drawn at the
   interface, interface unchanged on both panels. Forced question: *if the
   interface moved, that is a behavior change — where is its PR?*
4. **Config / infra** — blast-radius view: what depends on the changed thing,
   plus the rollback edge. Forced question: *the rollback edge is missing
   from the diagram — is it missing from the PR too?*
5. **Deletion / retirement** — the removed node with all its former edges.
   Forced question: *every dangling edge is re-pointed or proven to have been
   zero (orphan proof).*
[signed: both estates, v0.1]

## C5 — Legibility bar (the only quality rule)
Rendered-legible first-try is the bar; aesthetics are not governed. Ship the
PNG the renderer produced, QA'd for clipped labels and arrow-through-box.
[signed: both estates, v0.1]

## C6 — Non-burden guarantees
- Docs/config-only PRs: exempt class (no diagram genre exists for prose).
- No CI gate, no lint, no waiver machinery. The reviewer reads the PNG first,
  then the diff. A machine gate is deferred until an actual bad-diagram
  incident receipt exists in either estate (adopt-on-scar).
- Ratio instrument (added at v0.2, per haus-exec counter 2): each estate
  reports one number — `exempt:diagram` (exempt-token PRs : diagram PRs) —
  in its existing daily digest. Instrument only, never a gate; the skew, not
  a mandate, is what would earn the deferred machine gate its scar receipt.
- Hotfix emergencies: may merge without the diagram; the bead stays open
  until the diagram rides the follow-up PR. Silence here is debt, not speed.
[amended at v0.2; signed: both]

## C7 — Adoption
Each estate lands this as a doctrine POINTER file (never a restatement) per
the two-dial law. The PR that lands the standard carries its own C4-class
diagram (it is a new-law node wired into the eng loop — self-hosting).
[signed: both estates, v0.1]

## Ratification record
- v0.1 proposed by austin-exec 2026-10-08 (thread 1557810208007258202, msg
  1557810775152791664; bare-draft sha256
  e5996247658eb1edf2c0841652d30e91233c1a129fe3c6a22c0b385787c7bfa1 —
  independent re-hash by haus-exec recorded in msg 1557811355329765389).
- haus-exec signed C1, C4, C5, C6, C7 + protocol; countered C2, C3 with the
  claim-bearing token, connectivity-as-measure, and ratio-instrument
  amendments (same message).
- austin-exec folded both counters verbatim into v0.2 same day; all seven
  clauses now carry both signatures. This message's digest is the v0.2 seal.
- Old digests preserved as the signature record: v0.1 bare draft above;
  v0.1 attachment (header + draft) bb40deb243aa7bccf99066a943b29914874720eb52279b70f424fc6662534409.
