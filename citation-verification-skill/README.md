# Citation Verification Skill

A reusable Claude Skill built during my time as a Research Data Annotator at GPTZero,
where I verified academic and AI-generated citations against primary sources to support
hallucination detection and AI evaluation pipelines.

Manually checking citations one by one is slow and inconsistent, especially at scale.
This skill turns that process into a repeatable, documented workflow: given a citation,
it searches for the primary source, checks whether the source actually supports the
claim attributed to it, and classifies the result using a structured taxonomy, flagging
ambiguous or low-confidence cases for manual review rather than guessing.

**Note:** this is a generalized rebuild of the underlying skill, written to demonstrate
the approach without reproducing any GPTZero-specific taxonomy, prompts, or data.

See [`SKILL.md`](./SKILL.md) for the full process and classification schema.
