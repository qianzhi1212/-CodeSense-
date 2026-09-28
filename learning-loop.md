# CodeSense learning loop

This document describes the manual v0.1 experiment. Keep the stages separate so the learner's judgment and the AI review can be compared.

## 1. Select a real code problem

Use a small, real code change from an AI-assisted project. Capture the requirement, relevant code, source, and only the context needed to judge behavior. Avoid inventing a clean example just to make the exercise easy.

## 2. Record the learner's first judgment

Before reading AI feedback, write down:

- Whether you think the code has a problem.
- What the problem is and where the evidence appears.
- Why it matters relative to the requirement.
- What you are uncertain about.

This is the baseline. Preserve it unchanged.

## 3. Request an independent AI review

Ask the AI to review the requirement and code without using your baseline. Request concrete code evidence, reasoning, possible impact, and relevant knowledge areas. Ask it to state assumptions and uncertainty. Do not ask it to teach yet.

## 4. Compare and identify the knowledge gap

Compare your baseline with the review. Separate missed issues from disagreements and false alarms. Identify the smallest knowledge gap that explains a missed or weak judgment; do not turn every Case into a broad programming lesson.

## 5. Learn only what the gap requires

Study the relevant concept using the original code as context. Ask for a short explanation, a simple contrast, and a chance to explain the concept back in your own words. Keep the review available as feedback, not as a substitute for your reasoning.

## 6. Re-judge the original code

Set aside the AI's conclusion and revisit the requirement and code. Explain the issue, evidence, rationale, and limits in your own words. Record what changed from the baseline and what remains uncertain.

## 7. Generate and judge a variation

Create one meaningfully different scenario that still tests the same judgment ability. Do not reveal the intended answer before the learner commits to a judgment. Record the variation and the learner's reasoning. A second variation is optional when one result is ambiguous.

## 8. Record and continue

Use `results/_template-result.md` to record the baseline, AI feedback, learning, re-judgment, and transfer result. A correct answer on the original case alone does not establish transfer. Keep misses and uncertainty in the record, then select the next real Case.

