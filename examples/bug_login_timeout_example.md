# BUG: Login Timeout Under Load

- id: RB-142
- date-opened: 2026-04-20
- date-resolved: 2026-04-22
- owner: backend-team
- tags: #type-bug #priority-p1 #status-resolved #area-backend

## Symptom

Users experienced random login failures during peak traffic.

## Root Cause

DB connection pool reached max size due to long-running auth queries.

## Fix

- optimized auth query index
- lowered query timeout
- tuned pool size and retry policy

## Prevention

- added load test scenario for login
- added alert on pool saturation threshold
