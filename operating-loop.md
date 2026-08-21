# Operating loop

The system runs in cycles. One cycle should be cheap enough to run often.

## 1. Scan

`market-scout` generates candidate venture ideas from open-ended search. No niche
is supplied. Output: 10–20 one-line candidates in `state/backlog.md`.

Cost target: low. This is deliberately shallow.

## 2. Screen

`opportunity-analyst` scores candidates against the screen in
`docs/gates.md#screen-criteria`. Most die here. Survivors get a folder under
`ventures/`.

## 3. Research

`research-manager` commissions a real investigation for each survivor: demand
evidence, competitors, cost to reach first customer, why this is not already
done. Output: `ventures/<name>/research.md`.

`peer-reviewer` then attacks it. The review is appended to the same file.

## 4. GATE 1 — human

Manager writes a one-page recommendation to `state/decisions.md` marked
`AWAITING HUMAN`. You approve, reject, or ask for more. Nothing proceeds without
your word.

## 5. Build a test

`product-manager` and `builder` produce the smallest possible thing that
produces a real signal. Usually a landing page and an offer, not a product.

`qa-reviewer` checks it works and that the claims on it are defensible.

## 6. GATE 2 — human

Anything that costs money or goes public stops here. Always.

## 7. Measure

`growth-manager` runs the test. `finance-controller` logs every cost to
`state/ledger.md`. Results go to `ventures/<name>/metrics.md`.

## 8. Decide

Scale, iterate, or kill — written to `state/decisions.md` with reasoning. Killed
ventures keep their folder. The record of why something failed is an asset.

Then back to step 1.
