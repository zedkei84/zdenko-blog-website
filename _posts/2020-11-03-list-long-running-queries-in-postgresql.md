---
date: 2020-11-03 15:30:00
title: List long-running queries in PostgreSQL
categories:
  - Databases
description: How to list long-running queries in PostgreSQL
type: Document
---

## How to list long-running queries in PostgreSQL

The following SQL query will list all SQL queries running for longer than 5 minutes.

~~~sql
SELECT
  pid,
  now() - pg_stat_activity.query_start AS duration,
  query,
  state,
  wait_event_type,
  wait_event
FROM pg_stat_activity
WHERE (now() - pg_stat_activity.query_start) > interval '5 minutes'
ORDER BY duration DESC;
~~~

&nbsp;