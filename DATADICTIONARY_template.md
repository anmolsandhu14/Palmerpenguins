# DATA DICTIONARY (Template)

> **Generated on 2026-01-29**  
> _Fill in all bracketed fields. Remove guidance text before publishing._

---

## Purpose
A data dictionary provides variable‑level documentation so others can understand, evaluate, and reuse your data across files/tables. Place this file alongside your dataset (e.g., in `/docs` or the dataset root) and update it whenever variables change.

## Dataset / Project
- **Title**: [Dataset or project title]
- **Version**: [vX.Y.Z]
- **Maintainer(s)**: [Name, role, email, ORCID]
- **Data collection period**: [YYYY-MM-DD to YYYY-MM-DD]
- **Last updated**: [YYYY-MM-DD]

---

## Table of Contents
- [How to Read This Dictionary](#how-to-read-this-dictionary)
- [Global Conventions](#global-conventions)
- [Per‑Table/Per‑File Schemas](#per-tableper-file-schemas)
- [Code Lists / Controlled Vocabularies](#code-lists--controlled-vocabularies)
- [Change Log](#change-log)

---

## How to Read This Dictionary
Each variable entry uses the following fields:

- **Variable ID**: Short, stable identifier (no spaces).  
- **Variable Name (Label)**: Human‑readable label shown in headers/figures.  
- **Definition / Meaning**: Clear description of what the variable represents.  
- **Datatype**: e.g., integer, float, string, boolean, date, datetime, categorical.  
- **Format / Pattern**: e.g., `YYYY-MM-DD` (ISO 8601), regex like `^[A-Z]2[0-9]3$`.  
- **Units**: e.g., `mg/L`, `°C`; include conversions if common.  
- **Allowed Values / Range**: Enumerations or numeric bounds (inclusive/exclusive).  
- **Missing Codes**: e.g., `NA`, `-999` (and meaning for each).  
- **Derivation / Calculation**: Formula, script step, or provenance (cite source variables).  
- **Constraints / Validation**: Uniqueness, primary key, foreign key, required/not null, domain checks.  
- **Confidentiality / Sensitivity**: e.g., direct identifier, quasi‑identifier, de‑identification applied.  
- **Notes / QA**: Caveats, quality checks, anomalies, version notes.

> _Tip:_ Keep variable IDs machine‑readable (snake_case) and labels human‑readable.

---

## Global Conventions
- **Character encoding**: [e.g., UTF-8]
- **Decimal separator**: [.]  
- **Date/time standard**: [ISO 8601]  
- **Coordinate reference system (if spatial)**: [e.g., EPSG:4326]  
- **Language(s)**: [e.g., en, fr]

---

## Per‑Table/Per‑File Schemas

### File/Table: `[filename_or_table_name]`
**Description**: [Brief description of what this file/table contains]

**Row semantics**: [What does a row represent?]

**Primary key**: `[variable_id(s)]`  
**Foreign keys / links**: `[variable_id]` → `[other_table.variable_id]`

#### Variables

| # | Variable ID | Variable Name (Label) | Definition / Meaning | Datatype | Format / Pattern | Units | Allowed Values / Range | Missing Codes | Derivation / Calculation | Constraints / Validation | Confidentiality / Sensitivity | Notes / QA |
|---:|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | `[sample_id]` | `[Sample ID]` | [Unique identifier for a sample] | integer | n/a | n/a | ≥ 1; unique | NA | n/a | primary key; not null | low | [Any notes] |
| 2 | `[collection_date]` | `[Collection date]` | [Date sample was collected] | date | YYYY-MM-DD | n/a | 1900-01-01 to today | NA | n/a | not future date | medium (dates may be sensitive) | [QC: date range check] |
| 3 | `[temp_c]` | `[Temperature]` | [Ambient temperature at collection site] | float | n/a | °C | −50 to 60 | NA | n/a | numeric range | low | [Instrument calibration notes] |
| 4 | `[status]` | `[Status]` | [Processing state] | categorical | n/a | n/a | ('raw', 'cleaned', 'excluded') | NA | n/a | must be one of list | low | [Business rules] |

_Add rows as needed. Repeat this whole **Per‑Table** section for each dataset/file._

---

## Code Lists / Controlled Vocabularies
Provide definitions for categorical variables. Reference authoritative vocabularies where possible.

**Example:**

**`status` codes**  
- `raw` — [Collected but not processed]  
- `cleaned` — [Processed and validated]  
- `excluded` — [Removed; see Notes]

_Link to external vocabularies/ontologies if used._

---

## Change Log
Document edits to variables, domains, or meanings.

- [YYYY-MM-DD] **vX.Y.Z** — [What changed and why]
- [YYYY-MM-DD] **vX.Y.Z-1** — [What changed and why]

---

## Maintenance
- **Editing process**: [Who approves changes; review frequency]
- **Location**: [Where the authoritative copy lives]
- **Related docs**: [README.md, protocol(s), codebook, SOPs]

---

### Checklist (remove after completion)
- [ ] Every file/table documented
- [ ] Variable IDs and labels reviewed for clarity and consistency
- [ ] Datatypes, formats, and units specified
- [ ] Allowed values/ranges and missing codes defined
- [ ] Primary/foreign keys identified
- [ ] Confidentiality and sensitivity assessed
- [ ] Code lists/controlled vocabularies included or linked
- [ ] Change log initialized and version set

