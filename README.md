F1 Team Cost-Efficiency & Risk-Adjusted Performance Dashboard
A financial-efficiency model that cross-references each 2024 Formula 1 constructor's championship points against team revenue and operating profit (Forbes estimates) to score risk-adjusted performance per $10M of revenue.

Live dashboard: https://yashdesai241me320-max.github.io/f1-cost-efficiency-dashboard/

What this answers
Championship standings measure who won on track. They don't measure who got there efficiently. This project asks: which teams deliver the most competitive result per dollar of revenue, and which are taking on the most financial risk to do it?

Key finding
McLaren and Ferrari lead the grid on risk-adjusted, revenue-normalized performance — not just on raw points. Mercedes has the largest revenue base ($799M) and strongest operating profit ($202M) on the grid but ranks 4th, because its efficiency (points earned per dollar of revenue) is lower than McLaren's or Ferrari's. Four teams — Aston Martin, Alpine, Williams, and Sauber — posted 2024 operating losses, which pulls down their risk-adjusted score even where their on-track points are respectable relative to spend.

Methodology
Efficiency = (2024 Constructor Points / Revenue) × 10 → points earned per $10M of revenue.

Financial Stability = Operating Profit / Revenue → operating margin, used as a proxy for financial risk. A team burning cash to compete is a riskier commercial proposition than one that isn't, regardless of where it finishes.

Both metrics are min-max normalized to a 0–100 scale across the 10-team field, then blended:

Risk-Adjusted Score = (Efficiency Score × 70%) + (Financial Stability Score × 30%)
The 70/30 weighting treats on-track return per dollar as the primary signal, with financial stability as a risk overlay. Weights are adjustable in the Excel model (Calculations tab, cell B3).

Data sources
Metric	Source
2024 Constructor Points	Official FIA 2024 season standings (final)
2024 Revenue & Operating Profit	Forbes, "Formula 1's Most Valuable Teams 2025" (published Nov 20, 2025)
Forbes converted all 2024 figures to USD using Dec 31, 2024 exchange rates (£1 = $1.26, €1 = $1.04). These are third-party estimates compiled from public filings, private documents, and industry interviews — not audited team financials — so treat the underlying dollar figures as directionally accurate rather than exact.

Files in this repo
index.html — the interactive dashboard (leaderboard, revenue-vs-points bubble chart, efficiency bar chart, full data table). Pure HTML/CSS/JS, no build step, deployed via GitHub Pages.
F1_Cost_Efficiency_Dashboard.xlsx — the full financial model in Excel: raw data, formula-driven calculations, a 1-page chart dashboard, and a Power BI–ready data table with an import guide.
Tech
Dashboard: vanilla HTML/CSS/JS + Chart.js for the bubble and bar charts, hosted on GitHub Pages.
Model: Excel (openpyxl-built), fully formula-driven — every derived metric recalculates if the raw inputs change.
Author
Yash Desai — LinkedIn · GitHub
