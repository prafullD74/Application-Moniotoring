# DataDog
Metrics are numerical values that can trace anything about your environment over time, from latency to error rated to user signups.
Visualizing Metrics 
Alerts are simply setting a threshould in a monitor.when that threshold is breached, a notification is sent to the designated recipient.
A trace is used to track the time spent by an application processing a request along with the execution path taken.

Datadog 101: Site Reliability Engineer
May18@#2023thrs
Relic
Monitoring is the act of collecting regular data about systems so performance can be viewed and tracked.
Is our service online and available?
Is our service functioning correctly?
Is our service performing well? 

MTTD is the amount of time, on average, between the start of an issue and when teams become aware of it. This does not include time spent troubleshooting or fixing the issue.
MTTR is the average amount of time between when an issue is detected, and when systems are fixed and operating normally again. Ideally this includes both time spent fixing the issue, and implementing proactive steps to prevent it from happening again.

Observability is the practice of instrumenting systems to gather actionable data depicting not only when and where an issue occurred, but—more importantly—why it occurred.

Monitoring is a verb. It’s symptom-oriented. It can identify when something is wrong, and where. Observability is a noun. It’s a type of approach that lets you ask why something is wrong. It provides the flexibility to dig into “unknown unknowns” on the fly.

observability requires gathering a lot of performance data, called telemetry data. There are four distinct types of telemetry data, summarized by the acronym “MELT”: Metrics, Events, Logs, and Traces. 

Observability platforms ingest data from our services with agents. Agents are integrated into a service through a process called instrumentation. 

An agent is typically a small application, typically a file or few lines of code, that automatically collects data and sends it somewhere to be analyzed, such as an observability platform.

Alerts notify stakeholders when telemetry data surpasses a predefined threshold, indicating a need for attention.
The role of a synthetic monitor is to run into an issue before one of your users does. Think of a synthetic monitor like a program, or a bot, that attempts the same action(s) over and over again.
