# SLI/SLO

## Service Level Indicators (SLI)

- Success rate: percentage of 2xx responses on /upload
- Latency: p95 response time for /upload

## Service Level Objectives (SLO)

- 99.5% successful uploads over 30 days
- p95 latency <= 500 ms over 30 days

## Measurement

- Metrics collected via Prometheus (planned)
- Logs used for basic validation during demos
