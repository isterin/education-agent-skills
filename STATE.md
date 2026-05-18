# STATE.md — education-agent-skills

**Last updated:** 2026-05-18 (Session 5)

## What was done

Added 3 new skills across 2 existing domains (no new domains):

1. **systems-thinking/leverage-and-response-design** — Fills the action gap in the systems-thinking domain. Given a systems analysis (iceberg, mental models, agency circles), helps students and educators design a wise intervention using Meadows' 12 leverage points hierarchy. Checks for unintended consequences using systems archetypes (shifting the burden, fixes that fail), generates 2-3 alternative responses at different leverage levels, includes a proportionality check (systemic burdens should not fall on young people), and explicitly asks whether doing nothing or less is the wisest response. evidence_strength: moderate.

2. **systems-thinking/systems-wellbeing-impact-mapper** — Maps systemic forces shaping a wellbeing concern at school or community level using Bronfenbrenner's ecological model (nested systems) and social determinants of health thinking. Explicitly redirects individual explanations ("students lack resilience") to systemic framings ("the transition process provides no relationship continuity"). Generates structural interventions at multiple system levels. Includes a surveillance warning: mapping systemic forces is not the same as measuring individual students' wellbeing. evidence_strength: emerging (practitioner synthesis of established frameworks).

3. **questioning-discussion/perspective-taking-designer** — Designs structured perspective-taking activities with anti-projection guardrails. Distinguishes contextual perspective-taking (investigating what someone actually thought/felt, using evidence) from projection (imagining what we would feel in their situation). Four-phase sequence: context-building, perspective identification, exploration, synthesis. Assessment criteria focus on reasoning quality, not emotional performance. Safety check for perpetrator empathy. Developmental calibration via Selman's stages. evidence_strength: moderate.

Also:
- Restored `systems-wellbeing-impact-mapper` chain reference in `mental-model-mapper/SKILL.md` (the chain had been removed as a ghost reference in a previous session; the skill now exists).
- CI workflow updated: 142 → 145.
- CLAUDE.md updated: 145 skills.
- README updated: badge, description, MCP tool/prompt counts (149 tools, 145 prompts).

## What was verified

- All 3 description fields verified ≤250 characters via Python: 181, 185, 198 chars
- All chains_well_with targets confirmed to exist on disk before writing
- `python3 scripts/validate-skills.py`: 145 skills, 0 errors, 4 pre-existing warnings (line-length on unrelated skills)
- `python3 scripts/validate-registry.py`: 145 skills, 19 domains — valid
- `npx playwright test`: 20/20 pass
- `cd mcp-server && npm run build && npm test`: 16/16 pass
- Committed and pushed: 0c3ba84

## What's next

- Systems-thinking domain now has 7 skills: iceberg, aspirational iceberg, mental model mapper, ladder of inference, agency circles, leverage-response design, wellbeing impact mapper. A composite orchestrator linking these into a full inquiry arc is a logical next step.
- Perspective-taking designer is the only skill in questioning-discussion that deals with historical/cultural empathy — cross-domain with historical-thinking domain is a natural chain to explore.
- The wellbeing mapper's "do not individualise" principle has natural overlap with trauma-informed-practice-designer in wellbeing-motivation-agency — worth documenting as a cross-domain pair.
