# SOC-BruteForce-Detection
Detection &amp; Incident Response of Brute Force Attacks using SIEM (CSA Project)

## Objectives
- To simulate brute force attacks by generating multiple failed login attempts.
- To ingest system logs into a SIEM platform for monitoring.
- To create a correlation rule that detects multiple failed logins from a single IP.
- To analyze suspicious IP addresses using threat intelligence sources.
- To prepare an incident response playbook for brute force attacks.


## Tools & Technologies
- **SIEM Tool**: Splunk (or ELK Stack / Wazuh can be used as alternatives)
- **Operating System**: Linux (Ubuntu) / Windows Server
- **Threat Intelligence**: VirusTotal, AbuseIPDB
- **Log Sources**: Authentication logs (Linux: `/var/log/auth.log`, Windows: Event Viewer Security Logs)
- **Optional**: Wireshark or Zeek for network traffic analysis


## Implementation

  ### Step 1: Log Generation
   - Simulated brute force attempts by entering wrong SSH/Windows credentials multiple times.
   - Linux: Checked `/var/log/auth.log` for "Failed password" entries.
   - Windows: Checked Event Viewer → Security Logs for Event ID 4625 (failed login).


  ### Step 2: Log Ingestion into SIEM
   - Configured Splunk Universal Forwarder to collect system logs.
   - Ingested logs into Splunk index and verified log flow.

### Step 3: Correlation Rule / Search Query
   - Created a Splunk query:
  
