# README

# Security Engineering Roadmap
A hands-on, lab-based self-study roadmap toward a mid-to-senior 
security engineering role at a top-tier tech company. No courses. 
No passive learning. Every concept proven through building.

## Why this exists

Most security certifications teach you to pass a test.  
This roadmap is built around a simple loop:

**Build something → break it → detect it → document it.**

## Phase 1 — Networking

**Goal:** Understand networks deeply enough to find attackers in traffic.

Labs:
- [ ] Segmented home lab — pfSense, VLANs, DMZ, firewall rules from scratch
- [ ] Packet analysis lab — tcpdump + Wireshark, identify attacks in raw traffic
- [ ] IDS with Suricata — write custom rules, generate and detect real attack traffic
- [ ] WireGuard VPN — build from scratch, understand routing, NAT, iptables
- [ ] DNS sinkhole — Pi-hole, analyze query logs, understand DNS tunneling
- [ ] Attack and detect — nmap, hping3, C2 traffic, lateral movement captures

Key concepts covered:
- TCP/IP, TLS, DNS, HTTP/HTTPS deeply
- Network forensics from pcap files
- IDS rule writing and evasion
- Firewall architecture and zone-based security

## Phase 2 — Linux

**Goal:** Understand Linux as both an attacker and a defender.

Labs:
- [ ] System audit lab — fully document a machine from scratch
- [ ] Systemd detection service — custom daemon, journald logging, alerting
- [ ] auditd + ELK stack — ship logs, write detections, find attacks in logs
- [ ] Attack and detect loop — privesc, persistence, reverse shells, log tampering
- [ ] CIS benchmark hardening — implement every control, verify with lynis
- [ ] Honeypot — deploy Cowrie, watch real attackers, analyze their behavior
- [ ] WireGuard + dnsmasq — VPN server with private DNS
- [ ] LUKS encryption — encrypted volumes, keyfile auto-mount at boot

Key concepts covered:
- Linux internals — processes, memory, file descriptors, signals
- Privilege escalation paths and detection
- auditd rules and log forensics
- SELinux/AppArmor policy writing
- Incident response on a compromised Linux host

## Phase 3 — Cloud (AWS)

**Goal:** Attack and defend AWS environments at an enterprise level.

Labs:
- [ ] CloudGoat — intentionally vulnerable AWS, work through attack scenarios
- [ ] Cloud monitoring stack — CloudTrail, Config, GuardDuty, custom alarms
- [ ] IAM deep dive — build, break, and fix overly permissive roles
- [ ] Cloud incident response — compromised EC2, isolate, investigate, remediate
- [ ] IaC security — Terraform + Checkov/tfsec, find misconfigs before deploy
- [ ] Secrets management — Secrets Manager, rotation, why env vars are dangerous
- [ ] Container security — EKS attack surface, pod security, network policies
- [ ] SSRF to metadata service — understand why it's critical in cloud environments

Key concepts covered:
- AWS shared responsibility model
- IAM — identity policies, resource policies, SCPs, permission boundaries
- Cloud detection engineering
- SSRF in cloud environments
- Data security at scale — KMS, S3 security, encryption key management

## Phase 4 — AI Security

**Goal:** Understand the attack surface of AI systems and how to defend them.

Labs:
- [ ] Local LLM lab — run open source models, attack them (prompt injection, jailbreaking)
- [ ] RAG application attacks — indirect prompt injection, data exfiltration via prompts
- [ ] OWASP LLM Top 10 — build a demo exploit for each item
- [ ] Model evaluation — Garak, PromptBench, run security evaluations
- [ ] ML supply chain security — poisoned models, unsafe pickle files, HuggingFace risks
- [ ] LLM-powered app hardening — input validation, output filtering, sandboxing

Key concepts covered:
- Prompt injection and indirect prompt injection
- LLM jailbreaking techniques
- AI supply chain threats
- Securing LLM-powered applications in production
- OWASP Top 10 for LLMs

## Coding (parallel track)

Running alongside all four phases. 20–30 minutes daily.

- Neetcode 150 — working through every pattern
- Python tooling — building security tools not just using them
- Every lab automated in Python where possible

Progress: [ ] Easy fluent [ ] Medium reliable [ ] Hard stretch goal

## Labs Index

Every lab lives in its own repo with:
- What I built
- What broke and how I fixed it
- What I learned
- Evidence (screenshots, pcap files, log snippets, architecture diagrams)

| Lab | Phase | Repo | Status |
|-----|-------|------|--------|
| Segmented home lab | Networking | [link] | [ ] |
| Packet analysis | Networking | [link] | [ ] |
| Suricata IDS | Networking | [link] | [ ] |
| WireGuard VPN | Networking | [link] | [ ] |
| ... | ... | ... | ... |

## How I document each lab

Every lab repo follows the same structure:
```
lab-name/
├── README.md        # What it is, what I learned
├── setup/           # How to reproduce it
├── attacks/         # Attack scenarios I ran
├── detections/      # How I detected each attack
├── evidence/        # Screenshots, pcaps, log snippets
└── lessons.md       # What broke, what surprised me
```

*Building in public. Every lab documented as I go.*
