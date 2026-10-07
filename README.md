# Grant Salary Cost Estimator

A single-page tool that gives a **very approximate** salary cost for University of Edinburgh research grant applications. Edinburgh Research Office does the final costing.

**Live site:** https://mattnolan001.github.io/grant-salary-estimator/

## Use
Open `index.html` in a browser. It needs no server or build step. For each role, enter:
- grade and spine point
- start date
- duration in months
- FTE %

Costs are summarised by grant year (12-month blocks from the earliest role start). There is also a month-by-month breakdown. "Copy as table" copies the summary for pasting into Excel or Word. Your inputs are saved in the browser.

## Method
- Base salary: UoE full-time scale, from 1 Nov 2025. The Real Living Wage supplement is added on spine points 9–13.
- +30% on-costs.
- +4% compounded every 1 August after the scale date (first on 1 Aug 2026). This covers increments and inflation together, so there is no separate spine progression.
- Each month costs annual ÷ 12 × FTE. Partial months are pro-rated by days.

## Updating the scale
Edit the `CONFIG` block at the top of the `<script>` in `index.html`:
- `spine`, `rlwSupplement` and `grades`
- `scaleDate` and `scaleLabel`
- `onCostRate` and `upliftRate`, if the guidance changes

Source: https://www.docs.csg.ed.ac.uk/HumanResources/Pay/Full%20time%20UE02%20to%20UE10%20-%20April%2026.htm

The grade-to-point ranges (especially UE10's normal/contribution split) were read from the spreadsheet layout and should be checked against HR guidance.
