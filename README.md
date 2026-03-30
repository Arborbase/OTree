# OTree — Corporate Ownership Structure Visualization

**by [ArborBase](https://arborbase.io) — Built by Labsky Consulting LLC, New York**

> Visualize complex corporate ownership structures in minutes — not hours.
> Free to download. Works completely offline. Your data never leaves your computer.

---

## What is OTree?

OTree is a privacy-first, offline tool for visualizing corporate ownership structures. Load your ownership data from a CSV file and OTree automatically draws the full chart, calculates indirect ownership percentages, and lets you explore the structure interactively.

No account. No upload. No internet required after download.

---

## Who is it for?

- **Corporate lawyers** — M&A due diligence, group structure documentation
- **Compliance and AML officers** — beneficial ownership mapping, EU AML regulation
- **Company secretaries** — maintaining statutory records and group charts
- **Private equity analysts** — portfolio company structuring
- **Family office administrators** — wealth structure management
- **Accountants and auditors** — group structure audit and reporting

---

## Why OTree is different

| Feature | OTree | Visio / PowerPoint | Lucidchart |
|---|---|---|---|
| Calculates effective indirect % | ✅ Automatic | ❌ Manual | ❌ Manual |
| Time-aware (as-of date) | ✅ Yes | ❌ No | ❌ No |
| Works completely offline | ✅ Yes | ✅ Yes | ❌ No |
| Data stays on your computer | ✅ Always | ✅ Yes | ❌ Uploaded |
| Handles multiple parents | ✅ Yes | ❌ Limited | ❌ Limited |
| Free to download | ✅ Yes | ❌ Paid | ❌ Paid |
| No account needed | ✅ Yes | ❌ Required | ❌ Required |

---

## Key Features

- **Automatic chart generation** — load a CSV and the chart draws itself
- **Effective % calculation** — calculates indirect ownership across all levels automatically
- **Time-aware** — set any as-of date to see the ownership structure at that historical point
- **Multiple parent handling** — companies with more than one owner shown clearly
- **8 positioning presets** — Fishbone, Top-down, Compact, Spacious, Wide, Tall, Centered, Smart Hybrid
- **Save layouts** — save and switch between named manual arrangements
- **Save snapshot** — self-contained HTML with all data embedded, reopens without CSV
- **Minimap navigation** — thumbnail overview with click-to-jump for large structures
- **Search** — find and jump to any company instantly
- **Export** — PNG, PDF, and effective holdings CSV
- **Collapse and expand** — hide branches to focus on relevant parts
- **Right-click context menu** — path from root, all descendants, effective holdings
- **Privacy-first** — single HTML file, zero external dependencies, fully offline

---

## How to Use

### Step 1 — Download

OTree v3.0 is coming soon. Watch this repository or contact [hello@arborbase.io](mailto:hello@arborbase.io) to be notified on release.

### Step 2 — Prepare your data

Download the CSV templates and fill in your ownership data:

**ownership_template.csv**

| Column | Description | Example |
|---|---|---|
| parent_name | The owning company | Alpha Holdings |
| child_name | The owned company | Beta Corp |
| ownership_pct | Ownership percentage (number only) | 60 |
| date_start | When this relationship started | 1/15/2010 |
| date_end | When it ended — leave blank if still active | 12/31/2020 |

**companies_template.csv** (optional)

| Column | Description |
|---|---|
| company_name | Must match exactly with ownership CSV |
| dba_name | Trading name or abbreviation |
| country | Country of incorporation |
| currency | Functional currency |
| company_type | Listed / Private / Partnership / Trust etc. |
| notes | Any additional notes |

### Step 3 — Open and load

1. Open `OTree.html` in Chrome, Edge, Firefox or Safari
2. Click **Load Ownership CSV**
3. Optionally click **Load Company Data**
4. Set the **as-of date** to view any historical structure

### Step 4 — Navigate

| Action | How |
|---|---|
| Zoom | Scroll wheel |
| Pan | Click and drag background |
| Move a company | Click and drag the box |
| Collapse/expand | Click the +/− button |
| Highlight | Left-click a company box |
| Full details | Hover over any box |
| More options | Right-click any box |
| Search | Type in the search box |

---

## CSV Format Notes

- Dates accept M/D/YYYY, MM/DD/YYYY or YYYY-MM-DD
- Separator: tab or comma — auto-detected
- Company names with commas: wrap in double quotes e.g. `"Smith, Jones & Co"`
- Leave date_end blank for currently active relationships
- Company names are case-sensitive

---

## Privacy

OTree runs entirely in your browser. Your CSV files are read locally and never sent anywhere. No server, no cloud storage, no analytics, no account required. The source code is fully open and auditable.

---

## License

OTree uses a dual license from v3.0 onwards:

**Open source and non-commercial use — GPL v3**
Free for personal, academic, non-profit and open source use.
See [LICENSE-GPL.txt](LICENSE-GPL.txt) for full terms.

**Commercial use — ArborBase Commercial License**
Required for use in law firms, accounting firms, compliance teams, or any for-profit organization. Also required for embedding OTree in software you sell or license to others.
See [LICENSE-COMMERCIAL.txt](LICENSE-COMMERCIAL.txt) for full terms.
Contact [hello@arborbase.io](mailto:hello@arborbase.io) for commercial licensing.

### License History

| Version | License | Status |
|---|---|---|
| v1.0 | MIT — permanent and irrevocable | No longer distributed |
| v1.1 | MIT — permanent and irrevocable | No longer distributed |
| v3.0+ | Dual license — GPL v3 + ArborBase Commercial | Current |

### License FAQ

**Is OTree free?**
Yes — for personal, academic, non-profit and open source use under GPL v3.

**Do I need a commercial license?**
Yes if you use OTree in any for-profit organization — even for internal use only.

**What does a commercial license cost?**
- Individual Professional: $49/year
- Team (up to 5 users): $199/year
- Enterprise: Contact hello@arborbase.io

**Can I evaluate before buying?**
Yes — 30 day free evaluation. Contact hello@arborbase.io.

---

## Roadmap

- [x] CSV loading with tab/comma auto-detection
- [x] Automatic chart generation
- [x] Effective indirect % calculation
- [x] Time-aware as-of date filtering
- [x] Multiple parent handling
- [x] Minimap navigation
- [x] Positioning presets
- [x] Save and switch named layouts
- [x] Snapshot export with embedded data
- [ ] Ribbon navigation (v3.0)
- [ ] Keyboard shortcuts (v3.0)
- [ ] Date slider with animated timeline (v3.0)
- [ ] Subset tree view — focus on any company as root (v3.0)
- [ ] Style presets by country and level (v3.0)
- [ ] AI analytics — natural language queries (v3.0)
- [ ] Mobile optimised layout (v3.0)
- [ ] ETree — employee org chart tool (planned)

---

## Disclaimer

OTree is provided for informational and visualization purposes only. It does not constitute legal, financial or compliance advice. Users are solely responsible for the accuracy and completeness of the data they enter. Labsky Consulting LLC makes no warranties regarding accuracy, completeness or fitness for purpose of the tool or its output.

---

## Contact

**ArborBase — by Labsky Consulting LLC**
New York, NY
[hello@arborbase.io](mailto:hello@arborbase.io)
[github.com/Arborbase/OTree](https://github.com/Arborbase/OTree)

*Feature comparison based on publicly available information as of 2026. Subject to change.*
