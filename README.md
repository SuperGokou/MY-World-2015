# 🌎 “MY World 2015” – Interactive Dashboard  
_CS 171 • Lab 10_

D3.js visual exploration of the **United Nations “MY World 2015”** global
survey, which asked millions of people to rank the issues that matter most for
a better life (education, health, jobs, etc.).  
The dashboard lets you:

1. **Brush a date-range** selector to focus on any slice of responses  
2. **See total responses over time** (CountVis)  
3. **Break the sample down by age-groups** (AgeVis)  
4. **Rank the 16 development priorities by popularity** (PrioVis)

---

## ✨ Features

| Component   | Interaction | Insight |
|-------------|-------------|---------|
| **CountVis** (`#countvis`) | Brush/drag to set start- and end-date | How survey participation grew |
| **AgeVis** (`#agevis`) | Updates with brush | Age distribution of respondents |
| **PrioVis** (`#priovis`) | Hover bars to see exact counts | What people in the brushed period care about |

Two grey labels above the brush (`#time-period-min`, `#time-period-max`) always
show the currently selected date range.

---

## Tech stack

* **D3.js v7** – drawing & data joins  
* **Bootstrap 5.1** – responsive grid & typography  
* **Google Font _Neuton_** – headline serif font

No build tool or bundler: the page is plain HTML + JS modules.

---

## File structure

		├── index.html # main page (layout + script tags)
		├── css/
		│ └── style.css # custom colours, fonts
		├── js/
		│ ├── countvis.js # class CountVis (line chart + brush)
		│ ├── agevis.js # class AgeVis (bar/pie chart)
		│ ├── priovis.js # class PrioVis (horizontal bar chart)
		│ └── main.js # loads CSV, instantiates the three views
		└── data/
		└── myworld_2015.csv # cleaned UN survey (date, age, priority columns)
		
		
		
## Data source
* ** United Nations Millennium Campaign –
* ** MY World 2015 global survey (16 priorities, free download) https://www.myworld2015.org

* ** Data was filtered to remove incomplete records and saved as data/myworld_2015.csv for offline use.		