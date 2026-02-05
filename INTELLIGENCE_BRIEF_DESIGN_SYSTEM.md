# Symia Intelligence Brief - Design System

This document describes the visual design system used in the Symia Intelligence Brief UI. Use these specifications to generate PDF documents or other outputs with matching aesthetics.

---

## Color Palette

### Primary Colors
| Name | Hex | Usage |
|------|-----|-------|
| `--bk` (Black) | `#0A0A0A` | Dark backgrounds, primary text on light |
| `--wh` (White) | `#FFFFFF` | Light text on dark backgrounds |
| `--or` (Orange/Crimson) | `#B91C1C` | Brand accent, headers, highlights, CTAs |
| `--lt` (Light) | `#FAFAF8` | Light section backgrounds |

### Gray Scale
| Name | Hex | Usage |
|------|-----|-------|
| `--g3` | `#D4D4D4` | Secondary text on dark |
| `--g4` | `#A3A3A3` | Muted text, metadata |
| `--g5` | `#6B6862` | Body text on light backgrounds |

### Status/Badge Colors
| Status | Hex | Usage |
|--------|-----|-------|
| Success/Confirmed | `#22c55e` | Confirmed badges, quick wins, success |
| Warning/Inferred | `#f59e0b` | Warning, inferred, medium complexity |
| Error/Risk | `#ef4444` | Errors, high risk, isolated silos |
| Info/Primary | `#3b82f6` | LMS, SIS, Federal grants |
| Purple | `#a855f7` | CRM, Foundation grants |
| Teal | `#14b8a6` | State grants, Communication systems |

### Technology Maturity Colors
| Level | Hex |
|-------|-----|
| Emerging | `#ef4444` |
| Developing | `#f59e0b` |
| Established | `#84cc16` |
| Advanced | `#22c55e` |

### System Category Colors
| Category | Hex |
|----------|-----|
| Learning Management System | `#3b82f6` |
| Student Information System | `#3b82f6` |
| Human Resources Information System | `#22c55e` |
| Financial Management System | `#22c55e` |
| Enterprise Resource Planning | `#10b981` |
| Customer Relationship Management | `#a855f7` |
| Alumni & Advancement System | `#a855f7` |
| Research Administration System | `#8b5cf6` |
| Analytics & Business Intelligence | `#6b7280` |
| Identity & Access Management | `#6b7280` |
| Facilities Management System | `#64748b` |
| Library Management System | `#0ea5e9` |
| Communication & Collaboration | `#14b8a6` |
| Assessment & Testing Platform | `#f97316` |
| Academic Advising System | `#ec4899` |
| Other System | `#6b7280` |

### Grant Type Colors
| Type | Hex |
|------|-----|
| Federal Grant | `#3b82f6` |
| State Grant | `#14b8a6` |
| Foundation/Private Grant | `#a855f7` |
| Corporate Partnership | `#22c55e` |
| Internal Initiative | `#6366f1` |
| Consortium/Collaborative | `#f59e0b` |

---

## Typography

### Font Families
```
--serif: "Lora", Georgia, serif          // Headlines, body text
--mono: "Share Tech Mono", monospace     // Labels, badges, technical text
```

### Type Scale

| Element | Font | Size | Weight | Letter-Spacing |
|---------|------|------|--------|----------------|
| Organization Name | Serif | 28px | 900 (Black) | normal |
| Section Headers | Mono | 12px | 600 | 4-5px |
| Card Titles | Serif | 18-22px | 700-900 | -0.5px to -1px |
| Body Text | Serif | 15-18px | 400 | normal |
| Badges/Labels | Mono | 9-10px | 600-700 | 2-3px |
| Metadata | Mono | 10-11px | 400 | normal |
| Executive Summary | Serif | 22px | 400 | normal |

### Line Heights
- Body text: `1.8` to `2.0`
- Headlines: `1.2`
- Cards: `1.7`

---

## Layout & Spacing

### Section Structure
```
┌─────────────────────────────────────────────────────────────┐
│  Section (padding: 60px 48px)                               │
│  ┌─────────────────────────────────────────────────────┐    │
│  │  Container (max-width: 1200px, margin: 0 auto)      │    │
│  │  ┌─────────────────────────────────────────────┐    │    │
│  │  │  SECTION HEADER (mono, 12px, crimson)       │    │    │
│  │  │  ────────────────────────────                │    │    │
│  │  │  (2px line, crimson at 20% opacity)          │    │    │
│  │  │                                              │    │    │
│  │  │  Content Grid/Cards                          │    │    │
│  │  └─────────────────────────────────────────────┘    │    │
│  └─────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────┘
```

### Section Backgrounds (Alternating)
1. Light (`#FAFAF8`) - Executive Summary, Systems, Opportunities, ROI
2. Dark (`#0A0A0A`) - Pain Points, Data Silos, Actions/Roadmap, CTA

### Grid Layouts
- **Cards**: `grid-template-columns: repeat(auto-fit, minmax(300-350px, 1fr)); gap: 16-20px`
- **Two-Column**: `grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 32px`

---

## Component Patterns

### 1. Section Header
```
[SECTION TITLE]          ← Mono, 12px, uppercase, letter-spacing: 4px, crimson
═══════════════          ← 2px line, crimson at 20-30% opacity
margin-bottom: 36px
```

### 2. Badge/Tag
```css
font-family: monospace;
font-size: 9px;
padding: 4px 8-10px;
background: [status-color];
color: white;
text-transform: uppercase;
letter-spacing: 2px;
```

### 3. Card (Light Background)
```css
background: white;
padding: 24-28px;
border: 1px solid rgba(10,10,10,0.08);
```

### 4. Card (Dark Background)
```css
background: rgba(255,255,255,0.03);
padding: 24px;
border: 1px solid rgba(255,255,255,0.06);
```

### 5. Highlighted Callout Box
```css
background: rgba([accent-color], 0.04-0.06);
padding: 16-20px;
border-left: 3-4px solid [accent-color];
```

Examples:
- **Data Implications**: crimson accent (`#B91C1C`)
- **Business Value**: green accent (`#22c55e`)
- **Pain Points**: red accent (`#fc8181`)

### 6. Progress Bar (for Priority Scores)
```css
/* Container */
height: 4px;
background: rgba(255,255,255,0.1);

/* Fill */
background: crimson;
width: [priority_score * 10]%;
```

---

## Section Specifications

### Header Section
- Organization avatar: 72x72px square, crimson background, white initial
- Name: 28px serif black
- Badges row: org type (gray), tech maturity (color-coded), counts

### Executive Summary
- Light background
- Large serif text (22px, line-height: 2)
- Centered max-width: 900px

### Pain Points
- Dark background
- Grid of red-accented cards
- Each card: left border 4px `#fc8181`, text in gray

### Identified Systems
- Light background
- Card grid with:
  - System name (18px bold)
  - Vendor (11px mono, gray)
  - Category badge (color-coded)
  - Confidence badge (green=confirmed, amber=inferred)
  - Evidence (italic)
  - Integration notes (mono, small)

### Active Grants
- Light background
- Card grid with:
  - Program name + type badge
  - Focus area (crimson)
  - Funding amount (22px bold crimson)
  - Time period
  - Description
  - Data Implications callout (highlighted)
  - Source link

### Data Silos
- Dark background
- Cards sorted by priority_score (descending)
- Each shows:
  - Silo name
  - Status badge (isolated=red, partial=amber, integrated=green)
  - Priority score with progress bar
  - Data types as tags
  - Integration barriers

### Integration Opportunities
- Light background
- Cards with:
  - Title + systems involved tags
  - Quick Win badge (green, if applicable)
  - Complexity badge (green/amber/red)
  - Data flows description
  - Business Value callout (green accent)
  - Success metrics

### Immediate Actions & Roadmap
- Dark background
- Two-column grid:
  - Left: Immediate Actions (amber accent)
  - Right: Short-term Roadmap (green accent)
- Numbered items with colored left borders
- Long-term Vision box at bottom

### Key Risks
- Light background
- Grid of red-accented warning cards

### Watchtower Fit (Sales Highlight)
- Gradient dark background
- Centered crimson header
- Large italic quote-style text

### ROI Factors
- Light background
- List with green checkmarks

### CTA Footer
- Dark background
- Centered
- Primary CTA button: crimson background
- Secondary: transparent with border

---

## PDF Generation Notes

1. **Page Size**: A4 or Letter, with generous margins (48px equivalent)
2. **Page Breaks**: Before each major section
3. **Headers/Footers**: Include page numbers, date, "CONFIDENTIAL" watermark
4. **Images**: Organization logo if available
5. **Links**: Make source URLs clickable in PDF

### Recommended Section Order for PDF
1. Header (Org info, badges)
2. Executive Summary
3. Pain Points Identified
4. Identified Systems
5. Active Grants & Programs
6. Data Silos Analysis
7. Integration Opportunities
8. Immediate Actions & Roadmap
9. Key Risks
10. Why Symia Watchtower
11. ROI Factors
12. Next Steps / CTA

---

## Example JSON → PDF Field Mapping

```python
# Header
organization_name → Title
systems_discovery.organization_type → Type badge
intelligence_brief.technology_maturity → Maturity badge
systems_discovery.student_count_estimate → Student count
systems_discovery.employee_count_estimate → Employee count

# Content Sections
intelligence_brief.executive_summary → Executive Summary text
programs_grants.pain_points_identified → Pain Points cards
systems_discovery.identified_systems → System cards
programs_grants.active_grants → Grant cards
intelligence_brief.data_silos → Silo cards (sort by priority_score DESC)
intelligence_brief.integration_opportunities → Opportunity cards
intelligence_brief.immediate_actions → Immediate action items
intelligence_brief.short_term_roadmap → Roadmap items
intelligence_brief.long_term_vision → Vision statement
intelligence_brief.key_risks → Risk cards
intelligence_brief.watchtower_fit → Watchtower pitch text
intelligence_brief.estimated_roi_factors → ROI bullet points
```
