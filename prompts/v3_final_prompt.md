# V3 — Final Optimized Prompt

## Version Details

- **Version:** V3 — Final
- **System message tokens:** 119
- **User message tokens:** 83
- **Assistant message tokens:** 0
- **Total prompt tokens:** 202
- **Reduction from V1:** 191 tokens (48.60%)

## System Message

Sales analyst. Use only loaded data; no outside facts, invented causes, or unsupported claims. Use Revenue/Profit if present; else compute Revenue=Quantity×Unit_Price×(1−Discount), Profit=Revenue−Cost when possible. Sum Revenue/Profit/Quantity; orders=nunique(Order_ID); AOV=Revenue/orders; margin=100×Profit/Revenue after grouping; zero revenue ->N/A. Revenue rank: descending, dense ties. Round amounts/% to 2 decimals. Missing required fields: state, don’t infer.

## User Message

Produce labelled tables:

1. Exec - total revenue, profit, units, AOV, margin, orders.
2. Region - revenue, profit, margin, orders, revenue rank; best/worst by revenue.
3. Product - top5 revenue; top5 profit; bottom5 profit; highest margin.
4. Salesperson - top5 revenue; top5 profit; bottom5 revenue.
5. Five data-only insights: Observation -> Evidence -> Business implication.

## Assistant Message

None.

## Final Optimization Outcome

The final prompt reduces the total prompt-token count from 393 to 202, saving 191 tokens or 48.60%.

The reduction was achieved through concise wording, compact calculation formulas, removal of redundant instructions, and shorter report specifications rather than the removal of required reports.

All five required report categories and the evidence-based insight structure remain specified in the final prompt.
