---
description: 'Risk and mitigation documentation instructions for project management.'
applyTo: 'docs/risk-mitigation.md'
references: 
  - 'docs/quality-criteria/ooa/qc-risk-mitigation.md'
  - 'docs/kpi.md'
  - 'docs/bc.md'
---

# Risk & Mitigation Documentation Instructions

This file provides templates and instructions for documenting project risks and mitigations.

## Risk Identification and Documentation Process
1. Use the provided template to document each identified risk, ensuring that all relevant information is captured consistently.
1. Identify risk categories (e.g., Technical, Business, Security, Compliance, Operational).
1. For each risk:
   - Assign a unique ID using the format RSK-[CATEGORY]-[NUMBER] (e.g., RSK-TECH-001 for Technical, RSK-BUS-001 for Business, etc.)
   - Specify category, description, impact, likelihood, mitigation, and status
   - Reference quality criteria (see qc-risk-mitigation.md)
   - Reference KPIs (see docs/kpi.md)
   - Impact and likelihood should be rated on a scale of 1-5, where 1 is low and 5 is high.
1. Prioritize risks based on their impact and likelihood to determine which ones require immediate attention.
   - Priority Level is calculated based on likelihood * impact (e.g., High for scores 15-25, Medium for scores 5-14, Low for scores 1-4).
   - Sort the risk tables by priority level to focus on the most critical risks first.
1. Update the risk register as new risks are identified or mitigated.
1. Store files in `docs/` as `risk-and-mitigation.md` (e.g., `risk-and-mitigation.md`).
1. Create files in English; if product owner domain language differs, create a separate file with language code suffix (e.g., `risk-and-mitigation.<language_code>.md`) and include a translation terms section in the English file.


## Risk Tables by Category


## Template (Minimal):
```markdown
# Risk and Mitigation for [Insert Project Name]

## Metadata
| Key               | Value                             |
|-------------------|-----------------------------------|
| Id                | RISK                              |
| crossReference    | BC                                |

## Version Log
| Version | Date       | Description              | Author     |
|---------|------------|--------------------------|------------|
| 0001    | [Insert today date in format yyyy-mm-dd] | Initial                  | <Insert Author Name> |

### Technical Risks
| Risk ID        | Description         | Impact | Likelihood | Mitigation         | Status  |
|----------------|---------------------|--------|------------|--------------------|---------|
| RSK-TECH-001   | ...                 | 5   | 3     | ...                | Open    |

### Business Risks
| Risk ID        | Description         | Impact | Likelihood | Mitigation         | Status  |
|----------------|---------------------|--------|------------|--------------------|---------|
| RSK-BUS-001    | ...                 | 4   | 4       | ...                | Closed  |

### Security Risks
| Risk ID        | Description         | Impact | Likelihood | Mitigation         | Status  |
|----------------|---------------------|--------|------------|--------------------|---------|
| RSK-SEC-001    | ...                 | 5   | 2       | ...                | Open    |

### Compliance Risks
| Risk ID        | Description         | Impact | Likelihood | Mitigation         | Status  |
|----------------|---------------------|--------|------------|--------------------|---------|
| RSK-COM-001    | ...                 | 4   | 3       | ...                | Open    |

### Operational Risks
| Risk ID        | Description         | Impact | Likelihood | Mitigation         | Status  |
|----------------|---------------------|--------|------------|--------------------|---------|
| RSK-OPR-001    | ...                 | 3   | 4       | ...                | Closed  |

## Priority Assessment
| Risk ID        | Priority Level | Impact | Likelihood |
|----------------|--------|------------|----------------|
| RSK-BUS-001    | 16           | 4      | 4          |
| RSK-TECH-001   | 15           | 5      | 3          |
| RSK-COM-001    | 12           | 4      | 3          |
| RSK-OPR-001    | 12           | 3      | 4          |
| RSK-SEC-001    | 10           | 5      | 2          |
---
Update this file as you identify and manage new risks and mitigations.

```

optional sections for product owner domain language:
```markdown
## Terms Translation

| Original Term           | [Language] Translation         |
|------------------------|---------------------------|
| [Original Term 1]      | [Translation 1]            |
| [Original Term 2]      | [Translation 2]            |
```

