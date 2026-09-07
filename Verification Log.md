**NovaTech Data Verification Log**

**Student Name: Habiba Musa**  
**Date:** 2026-09-06

Instructions

Query each pre-indexed knowledge base using Quick Chat. For each question, record the expected answer, Q's actual response, and whether they match. Minimum 6 entries, with 2 per data knowledge base.

Verification Log

|  | Knowledge Base | Question Asked | Expected Answer | Q's Actual Answer | Match? | Notes |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
|  | NovaTech CRM Deals | How many rows are in the CRM deals dataset? | 499 rows. | 499 rows. | Yes | Expected from data dictionary and CSV row count. |
|  | NovaTech CRM Deals | How many deals were won and how many were lost? | Won: 315; Lost: 184\. | Won: 315; Lost: 184\. | Yes | deal\_stage\` has only Won and Lost. |
|  | NovaTech Marketing Campaigns | How many rows are in the marketing campaigns dataset? | 2,240 rows. | 2,240 rows. | Yes | Expected from data dictionary and CSV row count. |
|  | NovaTech Marketing Campaigns | What is the campaign response rate? | 27.2%, or 609 responses out of 2,240 leads | 27.2%, or 609 responses out of 2,240 leads | Yes | campaign\_response is 1 for responded and 0 for no response. |
|  | NovaTech Support Tickets | How many rows are in the support tickets dataset? | 3,000 rows. | 3,000 rows. | Yes | Expected from data dictionary and CSV row count. |
|  | NovaTech Support Tickets | How many unresolved support tickets have a blank resolved date? | 59 unresolved tickets. | 59 unresolved tickets. | Yes | \`ticket\_resolved\_date\` is blank for unresolved tickets. |
|  | NovaTech Reference Documents | What are the three dashboard views Sarah Chen requested? | Marketing Funnel, Sales Pipeline, and Customer Health. | Marketing Funnel, Sales Pipeline, and Customer Health. | Yes  | From the Dashboard Requirements Brief. |

 Cross-Check

\- **Fact verified:** Example: CRM deals row count is 499\.  
\- **Chat said:** The CRM deals dataset (**novatech\_crm\_deals.csv**) contains **499 rows** and 20 columns. 

