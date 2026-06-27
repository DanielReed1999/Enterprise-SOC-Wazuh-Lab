# Detection Cases

Planned detection-validation cases after the infrastructure and agents are operational.

## Case 001 - Password Spraying against Active Directory

Goal: verify Wazuh visibility for repeated authentication failures against domain users.

Expected evidence:
- Windows authentication failure events
- Source host and target username patterns
- Wazuh alert/event entries
- Analyst conclusion and mitigation notes

## Case 002 - SSH Brute Force against Linux Endpoint

Goal: verify Linux authentication telemetry from Debian/Xubuntu endpoints.

Expected evidence:
- Failed SSH login attempts
- auth.log entries
- Wazuh event parsing
- Source IP and attempted usernames

## Case 003 - Privileged Group Modification

Goal: detect risky identity changes such as adding a user to a privileged group.

Expected evidence:
- AD group membership change event
- Wazuh alert/event entry
- Affected user/group
- Analyst decision and response recommendation

## Case 004 - Privilege Escalation Indicators

Goal: validate telemetry for local privilege boundary changes.

Expected evidence:
- Local admin changes
- Service creation
- Scheduled task creation
- sudoers modification on Linux
- suspicious PowerShell or shell execution
