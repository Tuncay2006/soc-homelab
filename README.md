# Home SOC Lab

A personal home lab I built to practice SOC analyst workflows hands-on. Everything runs in Docker on a Kali Linux VM.

---

## Stack

| Tool | Role |
|------|------|
| Wazuh 4.14 | SIEM / Log management |
| TheHive 5.6.3 | Case management |
| Suricata | Network IDS |
| Sysmon | Windows endpoint logging |
| Windows 11 | Monitored endpoint |

---

## How it works

1. **Suricata** uses the pcap library to capture packets from the network interface, matches them against the Emerging Threats ruleset, and writes the results to `eve.json`
2. **Sysmon** collects Windows system logs via the Windows Event Viewer (process creation, network connections, file changes)
3. **Wazuh agent** gathers both Suricata and Sysmon logs and forwards them to the Wazuh manager
4. **Wazuh manager** analyzes the incoming logs, applies detection rules, generates alerts, and acts as the central point for all security event management
5. **TheHive** receives the alerts from Wazuh so that SOC L1 analysts can investigate and resolve incidents

---

## What I did

- Set up Wazuh + TheHive via Docker on Kali Linux
- Connected a Windows 11 agent with Sysmon
- Forwarded Suricata logs through Wazuh into TheHive
- Wrote a Python script to integrate Wazuh alerts with TheHive 5 API
- Analyzed PCAP files and triaged alerts end-to-end

---

## Screenshots
https://github.com/Tuncay2006/soc-homelab/tree/main/screenshots
