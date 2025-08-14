# MoMA Art Explorer Tool

An interactive, Excel-based dashboard to explore the Museum of Modern Art (MoMA) collection by **Nationality**, **Artist**, and **Minimum Year of Creation**, and to display the **earliest qualifying artwork** with rich metadata and an embedded image.

> Built with advanced Excel features: `XLOOKUP`, `TEXTSPLIT`, `TEXTJOIN`, `REGEXEXTRACT`, `FILTER`, `COUNTIFS`, `MINIFS`, `MAXIFS`, `TAKE`, `TRANSPOSE`, and `IMAGE`.

---

## 🚀 Features
- Dependent dropdowns for **Nationality → Artist**
- Dynamic **Min Year** filter
- Automatic selection of **earliest qualifying artwork**
- Rich metadata view (title, year, medium, dimensions, classification, department, acquisition date, on-view location)
- **Embedded artwork image** directly in Excel

---

## 📂 Repository Structure

---

## 🧰 Getting Started

### Prerequisites
- Microsoft **Excel** (Microsoft 365 or Excel 2021+) for full compatibility with `TEXTSPLIT`, `TAKE`, `HSTACK`, and `IMAGE`.

### Open the Workbook
1. Download this repository or clone it.
2. Open **`workbook/MoMA_OnView.xlsx`**.
3. Go to the **Art Explorer** sheet.
4. Use the **Nationality** and **Artist** dropdowns and enter a **Min Year** to explore.

> If images do not display, ensure your Excel version supports the `IMAGE` function and that you have an active internet connection (images are loaded via URLs).

---

## 🛠️ How It Works (User Flow)
1. **Select Nationality** → Filters the list of artists.
2. **Select Artist** → Displays artwork count and earliest/latest years.
3. **Enter Min Year** → Filters the artist’s works by year.
4. **View Earliest Artwork** → Automatically presents the earliest qualifying piece with full metadata and image.

---

## 🧪 Key Excel Techniques

**Lookup & Join**
- `XLOOKUP` to map `ConstituentID` → Artist names  
- `TEXTSPLIT` + `TEXTJOIN` to handle multiple IDs per artwork

**Cleaning**
- `REGEXEXTRACT` to derive a 4-digit year from textual dates  
- Find & Replace to normalize the **OnView** field

**Filtering & Metrics**
- `FILTER` + `SEARCH` for artist-level subsets  
- `COUNTIFS` with wildcards for artwork counts  
- `MINIFS` / `MAXIFS` for earliest/latest years

**Presentation**
- `HSTACK` + `TAKE` + `TRANSPOSE` to shape output  
- `IMAGE` to render the artwork inside a cell

See [`src/formulas.md`](src/formulas.md) for full snippets.

---

## 📈 Example Validation
For **Diego Rivera** (Mexico) with a minimum year of **1900**, the earliest work on display is **“Cubist Landscape.”**

---

## 🔄 Roadmap / Ideas
- Additional filters (medium, classification, acquisition date range)
- Error prompts and data validation for out-of-range years
- Live connection to MoMA feeds for real-time updates
- Power BI or web app version for broader access

---

## 📜 License
This project is released under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

## 🙌 Acknowledgments
- Dataset: MoMA Collection  
- Project brief inspired by Maven Analytics Guided Project

_Last updated: {{YYYY-MM-DD}}_
