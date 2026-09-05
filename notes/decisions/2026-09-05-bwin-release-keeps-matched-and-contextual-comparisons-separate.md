---
date: 2026-09-05
author: ibm-audit
status: active
title: "The bWIN release separates matched forecast scores from community task context"
task: BWIN_RELEASE
---

The release page will place new measurements on the locked EEGMMIDB task in one
table, and community models with different tasks or input requirements in another.
EEGNet and ShallowConvNet are freshly trained forecasting adaptations, with every
change from their classification architectures stated. LaBraM, BENDR, BrainBERT
and The Virtual Brain receive no forecast rank without a matched experiment.

The comparison uses 24 context samples followed by 64 future samples at 125 Hz.
The benchmark owner verified that the historical `data.window=64` denotes future
length, rather than total length after subtracting context. The release will state
that correction explicitly; prior run scores retain their own protocol labels.

A homepage release entry points to the new page while predecessor results remain
in place. Checkpoint links and performance statements are filled only from the
verified release artifact. The root coordinator signals the completed review
before publication through the existing Cloudflare Pages process.

The normal source build also incorporates the already committed `1e6565c`
Results/run-history layout and its canvas/CSS support, which had not been copied
to `docs/`. The deployment diff was reviewed explicitly. The current release
corrects its now-stale statement that no matched predecessor rescoring exists,
while distinguishing the five-person common holdout from common-split retraining.
During review, unmatched closing spans on architectural canvases and an extra
CSS closing brace were corrected. The release and homepage were visually
inspected through the local browser, and the generated 16-page link check passed.
