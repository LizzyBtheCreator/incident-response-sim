Incident Response Simulation (Home Lab)

**Goal:** Demonstrate end-to-end incident response skills in a controlled environment:
- Run a vulnerability scan (Greenbone/OpenVAS)
- Capture network evidence (Wireshark)
- Validate one finding, remediate, and **prove** risk reduction with a rescan
- Deliver a concise incident response report

## Lab Topology
- **Scanner:** Greenbone Community Edition (Docker on macOS)
- **Target:** Linux VM on the same LAN (UTM/VMware)
- **Tools:** Greenbone (GVM/OpenVAS), Wireshark, Docker, Git/GitHub

## Scope & Rules of Engagement
- Only systems I own/control in my home lab
- Single host or small subnet
- Non-disruptive testing

## Methods (High Level)
1. **Detect/Analyze:** Run “Full and fast” scan, export report; capture traffic in Wireshark during scan.
2. **Validate:** Correlate one finding with packet evidence.
3. **Contain/Eradicate/Recover:** Patch or harden; rescan.
4. **Post-Incident:** Summarize lessons learned, prevention steps.

## Results (To be filled after run)
- Top 3 findings + CVSS:
  - ...
- Remediation applied:
  - ...
- **Before → After:** CVSS reduced / finding closed

## Repo Structure
