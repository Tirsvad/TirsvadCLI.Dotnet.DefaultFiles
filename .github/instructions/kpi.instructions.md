---
description: "Instructions for KPI (Key Performance Indicator) tracking and reporting."
applyTo: 'docs/kpi.md'
reference: 'docs/quality-criteria/ooa/qc-kpi.md'
---

# KPI Instructions (Summary)
- Use the provided KPI markdown template / examples.
- Replace all placeholders with project-specific content.
- Ensure KPIs are specific, measurable, achievable, relevant, and time-bound (SMART).
- IDs for KPIs should follow the format `KPI-[Category shortname]-[Number]` (e.g., KPI-F-001).
- Store KPI files in `docs/` as `kpi.md`.
- Increment version numbers for significant changes; keep only the latest version in main, archive older versions
- Include metadata, version log (with date, author), and use tables for KPI tracking.
- Create files in English; if product owner domain language differs, create a separate file with language

## Template (Minimal):
```markdown
# Key Performance Indicators (KPI) for [Insert Project Name]
## Metadata
| Key               | Value                             |
|-------------------|-----------------------------------|
| Id                | KPI                               |
| crossReference    | FURPS                             |

## Change log
| Version | Date       | Description              | Author     |
|---------|------------|--------------------------|------------|
| 0001    | <today date in format yyyy-mm-dd> | Initial                  | <Insert Author Name> |

---

## KPI Tracking

### [KPI Category 1]
| ID | KPI Name           |  Description                     | Target Value | Current Value | Status  | Measurement Interval | Reference      |
|----|--------------------|----------------------------------|--------------|---------------|---------|--------------------|----------------|
| KPI-[Category]-[] | [KPI 1] | [Description of KPI 1]           | [Target Value] | [Current Value] | [Status] | [Interval] | [FURPS-ID]      |

```
