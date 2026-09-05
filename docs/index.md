# Privacy Skill Vault - Learn
Welcome to the Privacy Skill Vault Learning Platform
## Core Focus Areas
Security Operations & SIEM
Cyber Fraud Prevention
Privacy & Hardening
!!! tip "Getting Started"
Explore the learning curriculum using the navigation or built-in search. 

---

## Design System Preview (Phase 5 Validation)

### Admonition Suite

!!! security "SECURITY DIRECTIVE"
    Operational identity preservation requires strict network boundary enforcement. Never transmit unencrypted telemetry across untrusted transport boundaries.

!!! danger "OPSEC ALERT"
    Do not store raw API credentials, active session tokens, or private signing keys in documentation repositories.

!!! warning "THREAT INTEL"
    Adversaries target misconfigured public storage buckets and unassigned CNAME records. Regular zone audits are mandatory.

!!! info "TELEMETRY NOTE"
    Sysmon Event ID 1 (Process Creation) must capture parent process command lines and cryptographic hashes (`sha256`) to support detection engineering.

!!! tip "DETECTION TIP"
    Correlate Active Directory Event ID 4624 (Type 10) with perimeter authentications to identify concurrent session anomalies.

### Card Primitives

<div class="psv-card-grid">
  <div class="psv-card">
    <div class="psv-card__meta">Core Focus</div>
    <h4 class="psv-card__title">Detection Engineering</h4>
    <p class="psv-card__body">Construct resilient SIEM correlation logic, Sysmon instrumentation, and audit telemetry across enterprise operating systems.</p>
  </div>
  <div class="psv-card">
    <div class="psv-card__meta">Core Focus</div>
    <h4 class="psv-card__title">Fraud Analysis</h4>
    <p class="psv-card__body">Analyze automated account takeover vectors, synthetic identity networks, and transaction anomalies with data-driven workflows.</p>
  </div>
</div>

### Table & Code Formatting

| Telemetry Source | Event ID | Identification Purpose | Logging Requirement |
| :--- | :--- | :--- | :--- |
| **Microsoft-Windows-Sysmon** | `1` | Process Creation | Full CLI Capture + SHA256 |
| **Microsoft-Windows-Security** | `4625` | Account Logon Failure | Domain Controller Logs |


```bash
# Verify process integrity and active network sockets locally
ss -tulpn | grep -E ':(443|80|8000)\b'
```
