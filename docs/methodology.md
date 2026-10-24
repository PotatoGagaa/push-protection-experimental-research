# GitHub Push Protection Research

## Research questions

RQ1: How does observed push-blocking behavior vary across
selected secret pattern categories?

RQ2: Do controlled changes in representation or context
change the observed outcome?

RQ3: Are non-secret negative-control samples blocked?

## Experimental controls

- Use a dedicated public test repository.
- Use only synthetic, non-live test data.
- Do not use real credentials or production secrets.
- Record repository settings and test dates.
- Change one variable at a time.
- Record push output and supporting evidence.
- Repeat unexpected outcomes before interpreting them.

## Outcome classification

BLOCKED: The push attempt was rejected by Push Protection.
ACCEPTED: The push completed successfully.
ALERT_ONLY: The push completed, but a secret-scanning alert appeared.
INCONCLUSIVE: The result could not be reliably attributed.

## Important limitation

An accepted push is not automatically a detection failure.
Interpret each result against the documented support status,
token version, repository configuration, and test conditions.

## Metrics

Observed block rate =
blocked eligible test cases / eligible test cases executed.

Do not call this overall detection accuracy unless the ground
truth and eligibility criteria support that interpretation.
