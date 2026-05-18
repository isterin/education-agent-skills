# STATE.md — education-agent-skills

**Last updated:** 2026-05-18 (Session 4)

## What was done

Added the `inclusive-design` domain with 3 Universal Design for Learning (UDL) skills:

1. **udl-lesson-auditor** — Audits an existing lesson against all three UDL principles (engagement, representation, action/expression). Identifies specific access barriers, suggests concrete modifications ranked by impact, and respects stated teacher constraints.

2. **udl-options-designer** — Generates 2-3 specific alternatives per UDL principle for a given learning goal. Emphasises specificity (not "add visual supports" but the exact representation). Includes a minimum viable UDL recommendation — the one highest-impact change.

3. **udl-barrier-anticipator** — Predicts access barriers before delivery given a learner variability profile. Analyses engagement, representation, action/expression, environmental, and assessment barriers. Distinguishes barriers addressable through design from barriers requiring specialist support.

All three skills:
- evidence_strength: moderate (UDL is well-established as a design framework; implementation evidence is mostly quasi-experimental — no large RCTs for the complete framework)
- Cite: Rose & Meyer (2002), CAST (2018) UDL Guidelines v2.2, Meyer Rose & Gordon (2014), Ok et al. (2017) systematic review, Rao & Meo (2016), Edyburn (2010)
- No claims that UDL "ensures" or "guarantees" inclusion
- chains_well_with: all three UDL skills cross-link plus curriculum-assessment/differentiation-adapter, curriculum-assessment/formative-assessment-technique-selector, self-regulated-learning/self-regulation-scaffold-generator (all verified to exist on disk)

## What was verified

- All 3 description fields verified ≤250 characters via Python: 199, 219, 195 chars
- All chains_well_with targets confirmed to exist on disk
- `python3 scripts/validate-skills.py`: 142 skills, 0 errors, 4 pre-existing warnings (line-length)
- `python3 scripts/validate-registry.py`: 142 skills, 19 domains — valid
- `npx playwright test`: 20/20 pass
- `cd mcp-server && npm run build && npm test`: 16/16 pass
- CI workflow updated: 139 → 142
- CLAUDE.md updated: 142 skills, 19 domains, inclusive-design added to domain list
- README updated: badge, description count, domain table (19 domains), MCP tool count (146 tools, 142 prompts)
- Committed and pushed: 129d584

## What's next

- Session 5 candidates: another domain, or composite orchestrator linking UDL skills with differentiation-adapter and self-regulation-scaffold-generator
- EAL domain has natural overlap with UDL representation barriers — potential cross-domain chains worth documenting
