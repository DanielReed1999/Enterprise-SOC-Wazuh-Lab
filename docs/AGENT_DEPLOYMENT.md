# Wazuh Agent Deployment on Operating Systems

This lab uses Wazuh agents as the telemetry bridge between operating systems and the centralized Wazuh Manager.

## Deployed agent scope

| Agent name | Operating system | Asset role | Telemetry focus |
|---|---|---|---|
| `windows-server-dc` | Windows Server 2025 | Domain Controller / DNS / mail host | AD authentication, Kerberos, account and group changes, Windows Event Logs |
| `windows-10-vm` | Windows 10 Enterprise | Domain workstation | Logon/logoff, endpoint activity, local security events |
| `windows-11-vm` | Windows 11 Enterprise | Domain workstation | Logon/logoff, endpoint activity, local security events |
| `corp-web` | Debian 13 XFCE | Corporate web / Linux endpoint | auth.log, Apache, services, sudo, Linux system events |
| `admin-node` | Xubuntu Minimal | Administrator workstation | admin sessions, sudo, shell activity, Linux system events |

## Operational purpose

The agent layer is already part of the lab deployment. The next work is detection validation: trigger controlled events, confirm Wazuh ingestion, tune rules, and write analyst case notes.
