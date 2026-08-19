---
name: citation-verification
description: Verifies academic and AI-generated citations against primary sources and classifies their accuracy using a structured taxonomy, flagging ambiguous cases for manual review.
---

# Citation Verification Skill

## Purpose
Given a citation (author, title, publication, year, and any accompanying claim), determine
whether the citation is genuine and accurately represents its source, then classify it for
downstream use in research QA or AI-output evaluation.

## Process
1. **Locate the source.** Search academic databases, publisher sites, and DOI resolvers to
   find the primary source the citation refers to.
2. **Verify the claim.** Check whether the cited source actually supports the claim or
   statement attributed to it, not just that the source exists.
3. **Classify the result** into one of four categories:
   - Verified — source exists and supports the claim as stated
   - Verified with discrepancies — source exists but details (date, wording, attribution)
     don't fully match
   - Unverifiable — no matching source could be located with reasonable search effort
   - Fabricated — citation details do not correspond to any real source
4. **Flag ambiguous cases.** Where confidence is low (partial matches, ambiguous wording,
   paywalled sources that can't be fully checked), flag explicitly rather than forcing a
   classification, and note what would resolve the ambiguity.

## Output
A structured record per citation: classification, confidence level, and a short note on
what was checked and why the classification was assigned.
