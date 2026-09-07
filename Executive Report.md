 **NovaTech Revenue Intelligence Dashboard \- Executive Report**

**Prepared by:**  Habiba Musa  
**Date:** 2026-09-06

 **Executive Summary**

NovaTech's revenue data is split across CRM deals, marketing campaigns, and support tickets. The Revenue Intelligence Dashboard brings those datasets together around \`account\_id\` so Sarah Chen and the revenue team can review marketing performance, sales outcomes, and customer health in one place.

 **Business Problem**

The revenue team currently spends Monday meetings manually combining reports from three systems. This delays decision-making and leaves cross-functional questions unanswered, such as which campaigns produce closed deals and whether high-value customers are also high-support-risk accounts.

 **Data Sources**

| Dataset | File | Rows |  Purpose |
| :---- | :---- | :---- | :---- |
| CRM Deals | novatech\_crm\_deals.csv\` | 499 | Deal outcomes, sales reps, products, revenue, loss reasons |
| Marketing Campaigns | novatech\_marketing\_campaigns.csv | 2,240 | Campaign spend, responses, funnel stage, attributed revenue |
| Support Tickets | novatech\_support\_tickets.csv | 3,000 | Ticket priority, resolution time, product area, sentiment, risk indicators |

All three datasets share \`account\_id\`. Marketing and support include some orphan account IDs that do not appear in CRM; this should be noted as an intentional data quality issue.

 **Dashboard Design**

 View 1: Marketing Funnel

Recommended visuals:

\- KPI cards: total leads, response rate, attributed revenue, total campaign spend.  
\- Bar chart: response or conversion rate by \`campaign\_channel\`.  
\- Funnel visual or stacked bar: \`funnel\_stage\` by \`campaign\_channel\`.  
\- Combo chart: campaign spend vs. attributed revenue by \`campaign\_name\`.  
\- Table: campaign ROI by campaign and channel.

Recommended filters:

\- Campaign name  
\- Campaign channel  
\- Campaign date range  
\- Customer segment

 View 2: Sales Pipeline

Recommended visuals:

\- KPI cards: total deal value, win rate, average won deal value, total opportunities.  
\- Donut or bar chart: won vs. lost deals.  
\- Bar chart: loss reason count.  
\- Bar chart: revenue by \`company\_size\_tier\` and \`product\_category\`.  
\- Bar chart/table: win rate by sales region, sales rep, and product.  
\- Line chart: average days to close over time.

Recommended filters:

\- Sales region  
\- Sales manager  
\- Product line/category  
\- Deal closed date range  
\- Deal stage

 View 3: Customer Health

Recommended visuals:

\- KPI cards: total tickets, unresolved tickets, average resolution time, negative sentiment count.  
\- Bar chart: ticket volume by product area.  
\- Bar chart: average resolution time by priority.  
\- Sentiment breakdown by customer tier or region.  
\- At-risk accounts table: account ID/company, ticket volume, negative sentiment count, tickets last 30 days, total deal revenue.

Recommended filters:

\- Account  
\- Priority  
\- Product area  
\- Customer tier  
\- Region

 Calculated Fields

Possible calculated fields to create in Amazon Quick:

\- \`Win Rate\` \= won deals / total deals.  
\- \`Days to Close\` \= date difference between \`deal\_created\_date\` and \`deal\_closed\_date\`.  
\- \`Campaign ROI\` \= (\`revenue\_attributed\` \- \`campaign\_spend\`) / \`campaign\_spend\`.  
\- \`Response Rate\` \= average of \`campaign\_response\`.  
\- \`Resolution Time\` \= difference between \`ticket\_created\_date\` and \`ticket\_resolved\_date\`.  
\- \`At-Risk Flag\` \= high ticket volume \+ negative sentiment \+ high deal value.

 Initial Data Quality Notes

\- CRM contains 499 rows and 85 unique accounts.  
\- Marketing contains 2,240 rows and 150 orphan rows whose account IDs do not appear in CRM.  
\- Support contains 3,000 rows and 204 orphan rows whose account IDs do not appear in CRM.  
\- Marketing has 24 missing \`annual\_income\` values.  
\- Support has 59 missing \`ticket\_resolved\_date\` values because those tickets are unresolved.  
\- Lost CRM deals have \`deal\_value\` of 0 and blank \`loss\_reason\` for won deals is expected.

 Findings

\- Which channel has the strongest response/conversion rate? **Direct Mail** has the highest response rate at **53.02%**, significantly outperforming all other channels.   
\- Which products and segments drive the most won revenue?  **NovaPulse Launch** is the top-performing campaign with **138 conversions**,  nearly double the next closest campaign.   
\- Which product areas create the most support volume? **ACCT-041** leads by a wide margin with **334 support tickets**,  nearly double the next highest account. 

 **Recommendations**

Complete this after analysis. Possible recommendation types:

\- Shift budget toward channels with higher conversion or response rates.  
\- Investigate campaigns with negative ROI.  
\- Prioritize support improvements in product areas with high volume or long resolution times.  
\- Build an account review workflow for high-value accounts with negative sentiment and repeated tickets.

 **Appendix**

Include screenshots of:

\- Dataset upload/published status for all three CSV files.  
\- The three dashboard views.  
\- Quick Chat verification questions and answers.  
\- Q Exploration questions and dashboard cross-checks.  
