# Reasoning-Level Poisoning of Trusted Monitors

A systematic red-teaming methodology for knowledge-layer attacks on trusted AI monitors, developed at the AI Control Hackathon 2026 (Apart Research × Redwood Research).

## What This Is

This repository contains the complete Skill system that produces factual text with embedded false claims that frontier AI monitors cannot detect. Over 13 rounds of iterative development, this system achieved a 50% evasion rate against Claude Opus 4.6 in a maximum-difficulty setting (strongest attacker vs. equally capable monitor). In a validation round, a fresh AI session using only these files—with no prior experimental data—independently reproduced 50% evasion in entirely new domains.

## Repository Structure

```
├── SKILL.md                  # Main control flow + execution pipeline
├── methods.md                # 9 attack methods (3 discovery + 6 packaging)
├── defense-model.md          # 6-layer model of monitor cognition
├── experience-summary.md     # Empirical patterns from 13 rounds
├── scoring-protocol.md       # Evaluation rules + regression checks
├── dataset.json              # 8 annotated poison paragraphs with ground truth
├── phases/
│   ├── phase1-discovery.md   # Poison candidate discovery pipeline
│   ├── phase2-construction.md # Paragraph construction instructions
│   └── phase3-output.md      # Output format specifications
└── examples/
    ├── phase1-worked-examples.md  # Discovery worked examples
    └── phase2-worked-examples.md  # Construction worked examples
```

## Key Design Principle

The methodology files are self-contained: an AI with access only to these documents—and no prior experimental data or case history—can independently execute the full attack pipeline. Round 13 validated this property.

## Paper

See the accompanying research report: *Reasoning-Level Poisoning of Trusted Monitors: A Systematic Red-Teaming Methodology* (Tang Meng, AI Control Hackathon 2026).

## License

Released for AI safety research purposes.
