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

## What I did

- Set up Wazuh + TheHive via Docker on Kali Linux
- Connected a Windows 11 agent with Sysmon
- Forwarded Suricata logs through Wazuh into TheHive
- Wrote a Python script to integrate Wazuh alerts with TheHive 5 API
- Analyzed PCAP files and triaged alerts end-to-end

---

## Screenshots:
See [screenshots/](screenshots/)

---

## Docs to configuration :

