# RUNBOOK: Payment Gateway Timeout

- severity: sev1
- owner: sre-team
- tags: #type-runbook #area-infra #priority-p0

## Trigger

Error rate for payment API > 10% for 5 minutes.

## Immediate Actions

1. Enable fallback gateway route.
2. Throttle retries from checkout service.
3. Notify incident channel and assign commander.

## Verification

- payment success rate back above 97%
- p95 latency below 800ms

## Escalation

Escalate to gateway provider support if incident exceeds 15 minutes.

## Post-Incident Notes

Track root cause, customer impact, and required permanent fixes.
