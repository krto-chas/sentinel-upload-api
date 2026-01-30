# Runbook: Upload API Unavailable

## Symptoms

- /health returns non-200
- Elevated 5xx or timeouts
- Upload requests fail

## Triage

- Check CI status and recent deployments
- Check pod status: CrashLoopBackOff, OOMKilled
- Check logs for errors

## Mitigation

- Roll back to last known good deployment
- Restart pods if stuck
- Scale up if capacity issue

## Verification

- /health returns 200
- Upload succeeds with allowed file type
