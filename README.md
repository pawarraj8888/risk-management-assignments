# Risk Management Assignments

Homework for **FRE-GY 6123 Financial Risk Management** (NYU Tandon, Fall 2026), one folder per assignment.

**Site:** https://pawarraj8888.github.io/risk-management-assignments/

| Homework | Folder | Page | Author |
|---|---|---|---|
| 1. Treasury yield shocks, PV01 hedges and VaR | [`Homework 1`](Homework%201) | https://pawarraj8888.github.io/risk-management-assignments/homework-1/ | Rajvardhan Pawar |

## Layout

```
Homework 1/                    Excel workbook, written answers, docs (the page)
site/                          landing page of the site
.github/workflows/pages.yml    publishes the site
```

## How the site is published

On every push to `main` a GitHub Actions workflow copies `site/` and each homework's `docs/` folder into one
site: the landing page at the root and Homework 1 under `/homework-1/`. The workbook and the written answers
are copied next to the page as downloads. Nothing is built on the server. The pages are plain HTML with a
little JavaScript for the chart.
