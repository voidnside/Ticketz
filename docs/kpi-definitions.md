# KPI definitions

No KPIs are implemented yet. The current model contains staff users only, so it has no ticket or conversation data to measure. Define each metric before implementing it, including its time window, qualifying records, and edge-case behavior.

## Candidate metrics (not finalized)

| Metric | Candidate definition | Data needed | Open questions |
| --- | --- | --- | --- |
| First response time | Elapsed time from an inbound support conversation to the first qualifying agent reply | Conversation/message timestamps, direction, sender role, channel | Do automated acknowledgements count? Calendar hours or business hours? |
| Resolution time | Elapsed time from conversation creation to resolution | Conversation lifecycle timestamps and status history | How should reopened conversations count? |
| Workload by agent | Count of currently assigned open conversations per agent | Assignment and current status | How are unassigned or shared conversations handled? |
| Volume by channel | Count of conversations received through each supported channel in a period | Conversation channel and creation timestamp | How should merged or duplicate conversations count? |

These are proposals only. Final definitions depend on the ticket/conversation and message models, which are outside current scope.
