# Week 2 — Distributed Tracing

Watched week 2 Live stream and created notes with timestamps:

Timestamps:
`00:00 Introduction`

	- 00:42 AWS Ontario Virtual User Group
	- 01:42 Sponsors (Adrian Cantrill, WeCloudData, AWS)
	- 03:19 AWS User Groups Global
	- 03:34 Schedule
	- 03:43 Read the Instructions
	- 04:00 Guest Instructor Jessica Kerr & Student Advocate Shala Warner
	
`04:45 Programs & Softwares, Debugger & Observability, Logs vs Observability, Story by Logs is Tracing`

`08:45 Example of a Trace (Backend sequential queries on mysql through duration graph)`

`12:47 Service Map Honeycomb`

`14:00 Instrumentation (Code that sends data to make Trace)`

`15:33 Student Homework, Discord, Using Tags, Captioning unavilable in Youtube`

`21:28 Gitpod using week-2-again branch`

`23:44 Honeycomb.io Login`

	- 25:09 Environments
	- 27:16 Export Honeycomb API key Environment
	- 29:45 Set Service Name
	
`30:24 Hardcoding OTEL (Open Telemetry) service name env in docker compose for indivudual service`

`33:41 OpenTelemetry open source by CNCF, configurable, open standard of observability platform`

`37:29 Exporting env variables works for current shell tab and not accross parallel shell tabs`

`39:19 Instrumentation instructions`

`41:21 Step 1- Requirements.txt `

`45:04 Step 2- Initializer, OpenTelemetry for Python, Setting Env variables`

`51:52 Step 3- Configure & Run, Instrument Honeycomb`

`56:13 Why npm install is manually done when Dockerfile does it`

`57:00 Never use same Dockerfile in production & development`

`59:36 Staging vs Production Envirnment`

`1:00:05 Docker compose is up`

`1:01:23 Ports unlocked by default using gitpod.yml`

`1:04:00 Making API calls for Honeycomb to collect data, Debugging why data was not received, logging spans`

`1:09:40 Suggestion: Docker compose overwrites it with volume, getting spans after hitting endpoint`

`1:10:45 Resolution: Environment variables, API key not matching with ENV variable in container as it was copied from instructions`

`1:12:00 honeycomb-whoami.glitch.me to find out information about an API key like Team, Environment & permissions`

`1:14:30 honeycomb test env, setting correct API key env variable`

`1:20:29 Trace for single span, /api/activities/home`

`1:22:50 Hardcoding a span`

`1:23:30 backend_flask services > home_activities.py, tracer name home.activities`

`1:30:59 Fields & values in span, library name -> opentelemtry.instrumentation.flask`

`1:31:50 Adding attribute to span, make spans replacement for logs, creating custom span attributes`

`1:37:21 Honeycomb ui New Query, visualize->count, group by->trace.trace_id`

`1:40:40 Visualize trace, where -> app.result_length exists, visualize -> MAX(app.result_length)`

`1:43:30 Feature and billing comparison with Datadog`

`1:45:30 P90, Heatmap of query, zooming duration`

`1:47:48 Reason for adding observability early on in course, Distributed Tracing as a valuable skill on Resume`

`1:51:01 Committing code for homework, tagging using git`

`1:53:40 Homework Challenges discussion, new challenges over what is already done`
