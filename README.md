**AWS Log Search Recipes**

Battle-tested CloudWatch Logs Insights queries used during real production incidents.

When systems fail, dashboards lag and alerts lie.
Logs tell the truth — if you know how to ask.

🔍 What This Is

A curated collection of practical log search patterns designed for:

Cloud Engineers

DevOps & SREs

Platform teams

On-call responders

🟢 Free Example Recipe
Find the First Error in a Failure Cascade
fields @timestamp, @message, @logStream
| filter @message like /error|exception|failed/i
| sort @timestamp asc
| limit 20


Why it works:
Incidents have a temporal shape. The earliest error often introduces invalid state that cascades downstream.

📘 Full Handbook

40 production-ready recipes
Advanced incident reasoning patterns
Operational heuristics
Glossary & failure taxonomy

👉 Available here:
https://sogekey.gumroad.com/l/aws-log-search-recipes

⚠️ License

The full handbook is a paid product.
This repository contains sample material only.
