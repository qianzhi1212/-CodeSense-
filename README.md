# CodeSense

**Experimental / MVP v0.1** · A manual experiment in learning independent code judgment with AI-assisted review.

> **Status:** Experimental. The learning method has not yet been validated. The next step is to run Case 001 and record what happens.

CodeSense is a lightweight, case-based learning framework for people who want to understand code produced or changed with AI. It is not another automated code review product. It uses AI review as feedback, then asks the learner to explain the issue, revisit the original code, and try a related but different case.

## Core hypothesis

Structured AI-assisted review may help a beginner develop more independent code judgment when AI feedback is followed by targeted learning, a return to the original code, and a transfer check on a variation. This is a hypothesis to test, not a demonstrated result.

## Learning loop

```text
Real code and its requirement
        ↓
AI review
        ↓
Learner's first judgment
        ↓
Compare judgments and identify a knowledge gap
        ↓
Targeted learning
        ↓
Return to the original code and explain it independently
        ↓
Try a variation that tests the same judgment ability
        ↓
Make an independent judgment on the variation
        ↓
Record the result and choose the next case
```

For a useful baseline, write down your first judgment before reading the AI review. Then compare it with the review. The review should point to evidence and explain its reasoning; it should not replace the learner's judgment.

## What counts as a Case?

A Case is one **ability-training unit**, not just one code snippet or quiz question. It consists of:

- A real code problem and its relevant requirement or context (the case's core scenario).
- One specific code-judgment ability to practice.
- One clearly different variation by default (a second variation only when needed) to check whether the judgment transfers.

The variation should still exercise the same underlying ability while changing a meaningful condition. It should not merely rename variables or repeat the original example. See [the variation guide](docs/variation-generation.md).

## v0.1 scope

### Included in this manual MVP

- A documented, manually run learning loop.
- Case and result templates for recording the problem, first judgment, AI review, knowledge gap, learning, re-judgment, and transfer result.
- Guidance for generating and checking variations by hand with AI assistance.
- A small default: one variation per Case; add a second only when necessary.

### Not implemented

- Automated scanning or discovery of candidate cases.
- An automatic question or variation generator.
- IDE or GitHub integration, a web UI, or a standalone application.
- Evidence that this method improves code judgment.

## Run it manually

1. Choose a small, real change from an AI-assisted project and record its requirement and necessary context in a copy of [`cases/_template.md`](cases/_template.md).
2. Write your initial judgment before reading the AI review. Record evidence, reasoning, and uncertainty.
3. Ask an AI to review the code independently. Compare its findings with your baseline and identify the narrow knowledge gap.
4. Study only what is needed to understand that gap, then return to the original code and explain your judgment without relying on the review text.
5. Create one meaningfully different variation that exercises the same ability. Judge it independently, then record the outcome using [`results/_template-result.md`](results/_template-result.md).
6. Keep the record, including misses and uncertainty. Do not describe a Case as mastered solely because the original example now looks familiar.

See [`learning-loop.md`](learning-loop.md) for the full procedure and [`docs/mvp-scope.md`](docs/mvp-scope.md) for the v0.1 boundaries.

## Next step

Run **Case 001** on real code. Record the first judgment, AI review, learning gap, re-judgment, and variation result before changing the framework. The first run is an experiment, not proof that CodeSense works.

## Repository map

```text
learning-loop.md             Step-by-step manual workflow
cases/_template.md           Template for a real code Case
results/_template-result.md  Template for recording a learning run
docs/variation-generation.md Guidance for transfer variations
docs/mvp-scope.md            v0.1 included and excluded scope
```

## License

No license has been added in this experimental release. All rights remain with the copyright holder unless a license is added.

