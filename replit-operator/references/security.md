# Security scans

Open workspace Settings and select **Security**. Wait for the dependency-scan dashboard to render before concluding a scan is unavailable.

## Review

- Treat the dashboard as a workspace-wide view of dependency findings across projects.
- Use visible filters for severity, publishing status, and public visibility when narrowing scope.
- Prioritize publicly exposed projects and higher-severity findings, but do not take remediation action without approval.
- Treat displayed counts and last-scan information as live state, not durable knowledge.

## Run a scan

1. Verify the intended workspace and scan scope from the dashboard.
2. Activate **Run security scan** only when the user requests it.
3. Verify the request acknowledgement and the in-progress scan state.
4. Wait for results only when the user asks to monitor completion; otherwise report that the scan has been requested.

## Remediation boundary

**Fix with Agent** and similar actions can change projects. Explain the target project and planned modification, then obtain confirmation before starting any remediation.
