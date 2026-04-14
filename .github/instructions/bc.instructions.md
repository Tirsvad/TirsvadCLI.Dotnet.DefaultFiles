---
description: ' Business Case (BC) quality requirements and template for project documentation.'
applyTo: '/docs/bc.md' and '/docs/bc.*.md'
reference: 'docs/quality-criteria/ooa/qc-bc.md'
---

# DM Instructions (Summary)
- Use the provided BC markdown template / examples.
- Replace all placeholders with project-specific content.
- Store BC files in `docs/` as `bc.md`.
- Increment version numbers for significant changes and add it to the change log.
- Include metadata, version log (with date, author).
- Create files in English; if product owner domain language differs, create a separate file with language
- Use the provided BC markdown template / examples.

## BC Template (Minimal):
```markdown
# Business Case (BC) for [Insert Project Name]
## Metadata
| Key               | Value                             |
|-------------------|-----------------------------------|
| Id                | BC                                |
| crossReference    | [Insert Reference to DM or other relevant document] |

## Change log
| Version | Date       | Description              | Author     |
|---------|------------|--------------------------|------------|
| 0001    | [insert date of now in format yyyy-mm-dd] | Initial                  | [Insert Author Name] |

## Executive Summary
[Insert a brief summary of the business case, including the problem statement, proposed solution, and expected benefits.]

## Problem Statement
[Insert problem statement describing the issue or opportunity that the project aims to address.]

## Objectives

**Technical Requirements:**
- [Insert technical requirement 1]
- [Insert technical requirement 2]

**Business Requirements:**
- [Insert business requirement 1]
- [Insert business requirement 2]

**Phases:**
- First phase:
  1. [Insert first phase objective or deliverable]
  2. [Insert second phase objective or deliverable]
- Second phase:
  1. [Insert first phase objective or deliverable]
  2. [Insert second phase objective or deliverable]
- Third phase:
  1. [Insert first phase objective or deliverable]
  2. [Insert second phase objective or deliverable]

## Options and Alternatives (0-scenario, 1-scenario, 2-scenario)

## Cost Benefit Analysis
| Option | Cost | Benefit |
|--------|------|---------|
| 0-scenario | [Insert Cost] | No change, status quo maintained |
| 1-scenario | [Insert Cost] | [Insert Benefit] |
| 2-scenario | [Insert Cost] | [Insert Benefit] |

## Success Criteria
- [Insert success criterion 1]
- [Insert success criterion 2]

```

