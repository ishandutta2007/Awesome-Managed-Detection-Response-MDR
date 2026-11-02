# Awesome-Managed-Detection-Response-MDR

# Top Managed Detection & Response (MDR) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on 24/7 Human-Led Detection, MDR Platforms & Self-Hosted SOC Tooling*  
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Managed Detection & Response (MDR)**. These services and tools enable organizations to detect, investigate, and respond to cyber threats around the clock—combining automated detection with human expertise to contain incidents before they escalate.

**Examples** include CrowdStrike Falcon Complete, Arctic Wolf MDR, Red Canary MDR, Expel MDR, SentinelOne Vigilance, Rapid7 MDR, Mandiant Managed Defense, eSentire MDR, Secureworks Taegis MDR, and Sophos MDR (the category leaders).

**Open-source emphasis**: MDR is a domain where the **"managed" component is fundamentally a human service**—24/7 monitoring by expert analysts who investigate and remediate threats on your behalf. No open-source project replicates that service. What open-source *does* provide is **the tooling stack that MDR analysts use**: **Wazuh** is the leading open-source SIEM/XDR platform, and MDR providers like Graybox Security actually build their managed services on top of it . The **Wazuh + Cortex + TheHive** stack is a component-rich alternative for organizations building their own detection and response capabilities , while **Shuffle** provides a dedicated SOAR orchestrator for playbook automation . **XCLOAK Security Suite** offers an all-in-one open-source SOC platform combining SIEM, SOAR, EDR, DPI, and more . The critical caveat: **open-source gives you the tools, not the team**—managed detection and response is a service delivered by human analysts, and organizations without dedicated security staff should evaluate MDR providers rather than attempting to self-manage with open-source tools alone.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[CrowdStrike Falcon Complete](https://www.crowdstrike.com/)**  
  Fully managed MDR combining Falcon's endpoint protection with a 24/7 team that handles detection, investigation, and remediation on your behalf. The benchmark for managed endpoint security.

- **[Arctic Wolf MDR](https://arcticwolf.com/)**  
  Managed detection and response with a **Concierge Security Team** providing 24/7 monitoring, threat hunting, and response across endpoints, identities, and cloud.

- **[Red Canary MDR](https://redcanary.com/)**  
  Managed detection and response with **customer-validated 99% threat accuracy**; Q3 FY25 innovations include GenAI agent flows achieving **60%+ faster mean time to investigate** and a Security Data Lake for long-term retention.

- **[Expel MDR](https://expel.com/)**  
  MDR with **Ruxie** agentic AI that applies machine learning and structured reasoning to alerts—auto-closing benign noise and returning verdicts with full evidence in under 30 seconds.

- **[SentinelOne Vigilance](https://www.sentinelone.com/)**  
  Managed threat hunting add-on to SentinelOne's autonomous EDR; human analysts hunt for threats and respond on the customer's behalf.

- **[Rapid7 MDR](https://www.rapid7.com/)**  
  Managed detection and response combining InsightIDR with Rapid7's SOC team.

- **[Mandiant Managed Defense](https://www.mandiant.com/)**  
  Managed detection and response from Mandiant's incident response teams; combines front-line threat intelligence with continuous monitoring and hunting.

- **[eSentire MDR](https://www.esentire.com/)**  
  Managed detection and response service with 24/7 threat hunting.

- **[Secureworks Taegis MDR](https://www.secureworks.com/)**  
  Cloud-native XDR platform with managed detection and response services.

- **[Sophos MDR](https://www.sophos.com/)**  
  MDR with threat hunting, detection, and response integrated with Sophos endpoint protection; ITDR add-on (GA October 2025) extends coverage to identity threats.

## Open-Source GitHub Projects

### Full SOC Platforms (Wazuh)

- **[Wazuh](https://github.com/wazuh/wazuh)**  
  The **leading open-source SIEM/XDR platform** (GPLv2) and the foundation many MDR providers build on . Features: **intrusion detection**, **log data analysis**, **file integrity monitoring (FIM)**, **vulnerability detection**, **configuration assessment (SCA)**, **active response** for threat containment, and **regulatory compliance** reporting. **Recommended by practitioners** as the first choice for production environments requiring a free, self-hosted security platform. **Caveats**: requires a technical team for deployment, tuning, and maintenance; no real-time prevention (detection is log-based); the indexer consumes significant resources. **Best for organizations with security staff** wanting a comprehensive self-hosted platform—**not a replacement for managed MDR** if you lack the team to operate it.

### SOAR & Orchestration (Shuffle, TheHive + Cortex)

- **[Shuffle](https://github.com/Shuffle/Shuffle)**  
  Open-source **SOAR platform** with a visual workflow editor and a library of pre-built application connectors for rapid playbook construction without programming expertise . **Best for teams wanting dedicated automation orchestration**—but it is a SOAR tool, not a full detection platform.

- **[TheHive + Cortex](https://github.com/TheHive-Project/TheHive)**  
  Open-source **case management and observable analysis** stack. **TheHive** provides structured incident case management; **Cortex** runs analyzers for indicator enrichment. The combination with Wazuh represents a component-rich alternative to all-in-one platforms . **Caveat**: TheHive 5 is commercially licensed by StrangeBee with a free tier—TheHive 4 was AGPL-licensed fully open source. **Best for organizations building a modular SOC stack**.

### All-in-One SOC Platforms (XCLOAK)

- **[XCLOAK Security Suite](https://github.com/The-Abhishek1/XCLOAK-SECURITY-SUITE)**  
  Open-source **enterprise SOC platform** combining SIEM, SOAR, EDR, DPI, MDM, and NGFW in one self-hostable stack . Features: Go agents for autonomous collection across Linux and Windows (processes, connections, services, users, packages, FIM, registry persistence, cron jobs, kernel modules, SUID binaries, eBPF TCP events, passive DPI); detection engines covering TLS anomalies, HTTP inspection, protocol anomalies, port scans, exfiltration, JA3 fingerprints, credential attacks, privilege escalation, ransomware, and living-off-the-land techniques; UEBA with behavioral baselines; enterprise firewall with per-tenant policy . **Best for organizations wanting an integrated open-source SOC** in a single stack—but it is a newer project and requires operational expertise.

### Additional Strong Open-Source Options

- **AiSOC** — Open-source AI-powered SOC platform with alerts, cases, attack graph (Neo4j), MITRE heatmap, detection rules, UEBA, honeytokens, purple team testing, and compliance dashboards . **Best for teams wanting AI-augmented SOC capabilities**—but it is a large multi-service stack requiring significant infrastructure.
- **Sentora** — Open-source self-hosted AI-powered SIEM, EDR, and SOAR platform with per-verdict enrichment, threat feeds, air-gap mode, fleet exposure reporting, and agent config validation . **Best for organizations wanting an AI-native SOC platform**—but it is newer and less community-validated than Wazuh.
- **IMMUNE** — Open-source EDR/XDR/MDR platform in Pure C for DragonFlyBSD with kernel syscall hooks (execve, connect, bind, open, fork), cross-agent correlation, and automated playbook responses . **Best for researchers and DragonFlyBSD users**—not production-ready for most organizations.

**Frameworks for building custom systems**: For a **complete self-hosted SIEM/XDR foundation**, Wazuh is the mature standard and the basis for real MDR services . For **SOAR automation**, Shuffle provides visual playbooks . For **case management and enrichment**, TheHive + Cortex . For an **all-in-one SOC stack**, XCLOAK . **No open-source project provides managed detection and response**—that is a human service. Organizations requiring 24/7 MDR should evaluate CrowdStrike Falcon Complete, Arctic Wolf, Red Canary, Expel, or other MDR providers rather than attempting to self-manage with open-source tools alone.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- MDR platforms handling security telemetry must comply with organizational security policies and privacy regulations; **self-hosted SOC tools require skilled operators**—Wazuh, Shuffle, and TheHive are powerful but demand expertise to configure and interpret .
- **Open-source cannot replicate managed detection and response**—MDR is a service delivered by human analysts 24/7. Open-source provides **tools (Wazuh, Shuffle, TheHive)** but not the human expertise and continuous monitoring that define MDR. Organizations without dedicated security staff should not assume that deploying open-source tools constitutes "managed" detection—they should evaluate MDR providers.
- Verify license terms for commercial use; Wazuh uses GPLv2 , Shuffle uses AGPLv3 , and TheHive 5 has a commercial license with a free tier .

---

**Made for security leaders, SOC analysts, and organizations choosing their managed detection and response strategy.**  
Let's make detection and response more open at the tooling layer, but with clear eyes about the human expertise and 24/7 monitoring that managed services uniquely provide.
