**AWS Log Search Recipes**

Battle-tested AWS CloudWatch Logs Insights queries used during real production incidents.

When systems fail, dashboards lag and alerts mislead.
Logs tell the truth — if you know how to ask.

This repository shares a small selection of practical log search patterns designed for engineers working in production environments.

**What This Covers**

+ Failure cascades
+ Partial outages
+ Silent degradation
+ Authentication anomalies
+ Latency spikes
+ Incident reconstruction

These are patterns refined from real operational troubleshooting scenarios.

No theory.
No vendor fluff.
Just patterns that work.

🟢 **Example Recipe**
Find the First Error in a Failure Cascade -

fields @timestamp, @message, @logStream
| filter @message like /error|exception|failed/i
| sort @timestamp asc
| limit 20


**Why this works**

Incidents have a temporal shape. The earliest error often introduces invalid state that cascades downstream. Sorting chronologically surfaces the trigger instead of the noise.

**Who This Is For**

Cloud Engineers

DevOps & SREs

Platform Engineers

On-call responders

If you've ever stared at CloudWatch thinking
"I know the answer is in here somewhere" — this is for you.

**Full Handbook**

The complete collection contains:

40 production-ready log search recipes

Advanced incident reasoning patterns

Operational heuristics (what most engineers miss)

A practical failure-pattern glossary

Preview available here:

👉 https://bernalo.gitbook.io/bernalo-docs/aws-log-search-recipes-free-preview/

**License**

This repository contains sample material only.
The full handbook is a paid product.
