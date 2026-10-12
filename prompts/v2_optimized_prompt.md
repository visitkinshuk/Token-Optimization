# V2 — Optimized Prompt

## Version Details

- **Version:** V2 — Optimized
- **System message tokens:** 124
- **User message tokens:** 103
- **Assistant message tokens:** 0
- **Total prompt tokens:** 227
- **Reduction from V1:** 166 tokens (42.24%)

## System Message

Act as a sales-data analyst. Use only loaded data; no outside facts, invented causes, or unsupported claims. Use Revenue/Profit if present; otherwise, when possible, compute Revenue=Quantity×Unit_Price×(1−Discount), Profit=Revenue−Cost. Sum Revenue/Profit/Quantity; orders = nunique(Order_ID); AOV=Revenue/orders; margin=100×Profit/Revenue after grouping; zero revenue ->N/A. Rank revenue descending with dense ties. Round amounts/% to 2 decimals. Missing required data: state it, never infer.

## User Message

From the loaded sales file, return labelled tables:

1. Executive: total revenue, profit, units, AOV, margin, orders.
2. Region: revenue, profit, margin, orders, revenue rank; best/worst by revenue.
3. Product: top 5 revenue; top 5 profit; bottom 5 profit; highest-margin product.
4. Salesperson: top 5 revenue; top 5 profit; bottom 5 revenue.
5. Exactly 5 data-only actionable insights, each Observation → Evidence → Business implication.

## Assistant Message

None. A worked example remains unnecessary for the task.

## Changes from V1

- Replaced lengthy calculation explanations with compact formulas.
- Consolidated repeated instructions about unsupported claims and missing data.
- Shortened the descriptions of the five required reports.
- Retained aggregation rules, dense ranking, rounding, and all required outputs.
- Continued to omit the Assistant Message.

## Optimization Objective

Reduce prompt-token consumption while preserving the functionality and analytical safeguards required by the assignment.
