# Homework 1 - Treasury Yield Shocks, PV01 Hedges and VaR

**FRE-GY 6123 Financial Risk Management (NYU Tandon)** | Rajvardhan Pawar (rsp9234)

The data are two years of daily 2-year and 10-year Treasury yields (1-Oct-24 to 30-Sep-26), which give 521
daily changes in bp. The homework looks at how those changes are distributed, how the two yields move together,
how to hedge one note with the other using PV01, and the 99% 1-day VaR of a two-note portfolio.

Page: https://pawarraj8888.github.io/risk-management-assignments/homework-1/

| Sheet | What it has |
|---|---|
| `Sheet1` | the data as provided, unchanged |
| `Summary` | name and NetID, every answer in one table, the assumptions and the VaR method |
| `Q1-Q4 Stats` | share of changes within 1 and 2 SD, the correlation, conditional means, and the correlation on days when both changes are more than 1 SD from the mean |
| `Q5-Q7 VaR` | PV01 hedge, the equal-PV01 portfolio, the daily repricing of both legs and the 99% 1-day VaR |
| `Q8 VaR Graph` | VaR of $15 million 2-year + A million 10-year for A from -10 to 10, with the chart |

Files: [`rsp9234_rajvardhan_pawar_HW1.xlsx`](rsp9234_rajvardhan_pawar_HW1.xlsx) (workbook) and [`rsp9234_rajvardhan_pawar_HW1.docx`](rsp9234_rajvardhan_pawar_HW1.docx) (written answers).
Blue numbers in the workbook are typed inputs and everything else is a formula.

## Answers

| Question | Answer |
|---|---|
| 1 | 2-year: 73.90% within 1 SD, 95.20% within 2 SD. 10-year: 72.74% and 94.24% |
| 2 | Correlation 0.8204 |
| 3 | E[2-year \| 10-year >= 0] = 2.94 bp, E[10-year \| 2-year >= 0] = 3.22 bp |
| 4 | 96 days, correlation 0.9459 |
| 5 | Sell $78.62 million face of 2-year notes |
| 6 | $3.816 million face of 10-year notes. Equal PV01 is not equal risk |
| 7 | 99% 1-day VaR of $66,844 |
| 8 | Lowest VaR at A = -2.75 ($19,533), not at zero PV01, which is A = -3.816 ($20,106) |

VaR is by historical simulation: each of the 521 historical pairs of yield changes is applied to today's
position, both legs are repriced with the second-order formula, and the VaR is minus the 1st percentile of the P&L, shown as a positive loss.
