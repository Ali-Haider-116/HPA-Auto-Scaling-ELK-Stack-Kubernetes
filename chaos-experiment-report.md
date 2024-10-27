# Chaos Engineering Experiment Report

## Tools Used
- LitmusChaos

## Experiments Conducted
1. Simulated pod crash for `mysql` pod.
2. Introduced network latency for `client` pod.

## Issues Discovered
- MySQL pod took longer than expected to recover after crash.
- Increased latency affected client requests.

## Recommendations
- Improve readiness and liveness probes for quicker recovery.
- Implement circuit breakers for better fault tolerance.
