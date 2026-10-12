# Prompt Optimization Comparison

## 1. Overview

This experiment evaluated three versions of a prompt designed to generate five management reports from a sales dataset. The objective was to minimize prompt-token consumption while retaining the required reports, calculation instructions, and evidence-based insight structure.

## 2. Token Comparison

| Metric | V1 — Initial | V2 — Optimized | V3 — Final |
|---|---:|---:|---:|
| System message tokens | 190 | 124 | 119 |
| User message tokens | 203 | 103 | 83 |
| Assistant message tokens | 0 | 0 | 0 |
| **Total prompt tokens** | **393** | **227** | **202** |
| Tokens saved vs. V1 | 0 | 166 | 191 |
| Reduction vs. V1 | 0% | 42.24% | 48.60% |

## 3. Optimization History

### V1 — Initial Prompt

The initial version used detailed instructions to define analytical boundaries, calculation formulas, aggregation logic, ranking, rounding, missing-data handling, and the five report requirements.

**Baseline:** 393 tokens.

### V2 — Optimized Prompt

The second version reduced verbosity by replacing lengthy explanations with compact formulas, consolidating repeated safeguards, and shortening the report descriptions.

**Result:** 227 tokens, a reduction of 166 tokens (42.24%) compared with V1.

### V3 — Final Prompt

The final version further shortened role wording, report labels, and connecting phrases while retaining the specified analytical rules and report structure.

**Result:** 202 tokens, a reduction of 191 tokens (48.60%) compared with V1.

## 4. Optimization Summary

| Transition | Tokens Before | Tokens After | Tokens Saved | Reduction |
|---|---:|---:|---:|---:|
| V1 → V2 | 393 | 227 | 166 | 42.24% |
| V2 → V3 | 227 | 202 | 25 | 11.01% |
| V1 → V3 | 393 | 202 | 191 | 48.60% |

## 5. Functional Requirements

The final prompt retains instructions for:

- Executive sales summary
- Regional performance
- Product performance
- Salesperson performance
- Five evidence-based management insights

It also specifies calculation formulas, aggregation rules, descending dense ranking, rounding, and handling of missing fields.

## 6. Token Measurement

Token counts were measured using the OpenAI Tokenizer with the GPT-4o / `o200k_base` selection, as documented in the assignment. Counts apply to the raw System and User messages; the dataset and repository documentation are excluded.

## 7. Conclusion

The final prompt reduced the token count from 393 to 202, saving 191 tokens (48.60%). The optimization focused on concise wording and removal of redundancy rather than intentionally eliminating required analytical functionality.

The reported token reduction demonstrates prompt-length efficiency; it does not independently establish improved analytical accuracy, response speed, or monetary savings.
