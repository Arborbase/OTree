# OwnershipChart

**An offline, privacy-first tool for visualizing complex corporate ownership structures.**

Free to download and open source. No account needed. No data upload. Just open the file in your browser and load your data.

> The downloadable version is free and open source under MIT license. A hosted version with additional features is planned for the future.


---

## Screenshots

![OTree Welcome Screen]

![OTree Chart View]

![OTree Tooltip]

![ownership_template]

![companies_template]


---

## Who is this for?

- Corporate lawyers managing holding structures
- Company secretaries tracking subsidiaries
- Accountants and auditors mapping group entities
- Compliance officers visualizing beneficial ownership
- Private equity and family office administrators
- Anyone who has ever tried to draw a corporate structure in Excel or PowerPoint and eventually given up

---

## What it does

- Draws a **fishbone-style or curved line-style ownership chart** — parent companies on the left, subsidiaries branching right and downward
- Shows **ownership % on every line**
- Calculates **indirect / effective holding %** automatically (e.g. A owns 60% of B, B owns 50% of C → A effectively holds 30% of C)
- Handles **multiple parents** — companies owned by more than one shareholder are clearly shown with separate lines
- **Time-aware** — set an as-of date and the chart shows only the ownership structure that was active on that date
- Works with **300+ companies** — zoom, pan, drag nodes, collapse and expand branches

---

## Why it is different

| Feature | OwnershipChart | Visio / PowerPoint | Lucidchart | Cap table tools |
|---|---|---|---|---|
| Calculates effective % | ✅ | ❌ | ❌ | Partial |
| Time-aware (as-of date) | ✅ | ❌ | ❌ | ❌ |
| Data stays on your computer | ✅ | ✅ | ❌ | ❌ |
| Works offline | ✅ | ✅ | ❌ | ❌ |
| No account needed | ✅ | ✅ | ❌ | ❌ |
| Free to download, no account | ✅ | ❌ | ❌ | ❌ |
| Handles 300+ entities | ✅ | Hard | ✅ | ✅ |

**Privacy is the core design principle.** Your ownership data never leaves your computer. There is no server, no database, no analytics. The tool runs entirely in your browser.

*The downloadable open source version is free. Future hosted and team features will be available as paid plans.*

---

## How to use

### Step 1 — Download
Download `ownership_chart.html`, `ownership_template.csv` and `companies_template.csv` from this repository.

### Step 2 — Prepare your data
Open `ownership_template.csv` in Excel and fill in your ownership relationships:

| Column | Description | Example |
|---|---|---|
| `parent_name` | The owning company | Alpha Holdings |
| `child_name` | The owned company | Beta Corp |
| `ownership_pct` | Ownership percentage | 60 |
| `date_start` | When this relationship started (MM/DD/YYYY) | 01/15/2010 |
| `date_end` | When it ended — leave blank if still active | 12/31/2020 |

Optionally (but very powerful way to enrich the chart) fill in `companies_template.csv` with company attributes:

| Column | Description |
|---|---|
| `company_name` | Must match exactly the names in your ownership CSV |
| `dba_name` | Trading name or abbreviation |
| `country` | Country of incorporation |
| `currency` | Functional currency |
| `company_type` | Listed / Private / REIT / Startup etc. |
| `notes` | Any other notes |

### Step 3 — Open and load
1. Open `ownership_chart.html` in Chrome, Edge, Firefox or Safari
2. Click **Load Ownership CSV** and select your file
3. Click **Load Company Data** (optional) for attributes
4. Set the **as-of date** to see the structure on any date

### Step 4 — Navigate
| Action | How |
|---|---|
| Zoom in/out | Scroll wheel |
| Pan the chart | Click and drag the background |
| Move a company box | Click and drag the box |
| Collapse/expand branch | Click the +/− button on the box |
| Highlight connections | Click a box |
| Full details | Right-click a box |
| Search | Type in the search box |
| Export effective % | Click Export % button |

---

## Chart controls

| Control | What it does |
|---|---|
| **As-of date** | Filter relationships to a specific date |
| **Search** | Find and jump to any company |
| **Line style** | Switch between curved and fishbone lines |
| **Parent gap** | Adjust spacing between multiple owner lines (S/M/L) |
| **Lock layout** | Freeze positions so date changes do not move your layout |
| **Auto-spread** | Reset all positions to auto-layout |
| **Export %** | Download effective holdings as CSV — from highlighted company or root |
| **Collapse all / Expand all** | Show or hide all branches at once |

---

## Data format notes

- Dates must be in **MM/DD/YYYY** format
- Ownership % should be a number without the % sign (e.g. `60` not `60%`)
- Leave `date_end` blank for currently active relationships
- Company names are case-sensitive and must match exactly between the two CSV files
- One row per ownership relationship — if a company has two parents, it has two rows

---

## Example

A simple three-level structure:

```
ownership_template.csv

parent_name,child_name,ownership_pct,date_start,date_end
Global Holdings,Asia Corp,100,01/01/2010,
Global Holdings,Western Corp,100,01/01/2012,
Asia Corp,Trading Ltd,75,06/01/2015,
Asia Corp,Property Ltd,100,06/01/2015,
Western Corp,Energy Inc,60,03/01/2016,
Trading Ltd,Logistics Co,51,01/01/2018,12/31/2022
```

---

## Frequently asked questions

**Is my data safe?**
Yes. The tool runs entirely in your browser. Your CSV files are read locally and never sent anywhere. There is no server, no cloud storage, no analytics tracking.

**Does it work without internet?**
Yes — completely offline once downloaded. No external libraries are loaded.

**How many companies can it handle?**
Tested with 300+ companies. Performance depends on your computer but should be smooth up to 500+ entities.

**Can I add more company attributes beyond the 5 default columns?**
Yes — add any column you want to the companies CSV. The tooltip will display all columns automatically.

**What browsers are supported?**
Chrome, Edge, Firefox and Safari. Internet Explorer is not supported.

**Is OTree free?**
The downloadable open source version is free and will remain open source under MIT license. A hosted version with team features and cloud storage is planned as a paid product in the future.

**Can I share this with my team?**
Yes — share the HTML file and your CSV templates. Each person loads their own data. Nothing is shared between users unless you share the CSV files directly.

---

## Roadmap

- [ ] Multi-language support
- [ ] Color coding by country or entity type
- [ ] PDF/PNG export of the chart
- [ ] Password protection for sensitive charts
- [ ] Mobile responsive layout

---

## Disclaimer

OTree is provided for informational and visualization purposes only. It does not constitute legal, financial or compliance advice. Users are solely responsible for the accuracy and completeness of the data they enter. The developer makes no warranties, express or implied, regarding the accuracy, completeness or fitness for purpose of the tool or its output. Use of OTree does not create any professional advisory relationship between the user and the developer.

---

## Contributing

Feedback, bug reports and feature requests are welcome. Open an issue or submit a pull request.


---

## License

MIT License — free to use, modify and distribute. Attribution appreciated.

Copyright 2025 OTree
---

*Built with HTML, CSS and vanilla JavaScript. No frameworks. No dependencies. No nonsense.*
*The downloadable version is free  and open source. Always. Future hosted features will be offered as paid plans.*
*The downloadable version is free and open source. Always. Future hosted features will be offered as paid plans.*

*Feature comparison based on publicly available information as of 2025. Subject to change.*

