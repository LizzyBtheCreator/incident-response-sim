# Incident Response Simulation – Home Lab

**Date:** 2025-08-21  
**Author:** Elizabeth McMillan

## Executive Summary
One paragraph: what you scanned, key risk(s), what you changed, outcome.

## Scope & Method
- Targets: Sanitized IP (note: IP changed during DHCP; same machine)
- Tools: Greenbone CE (OpenVAS), Wireshark
- Approach: Full and fast scan → capture packets → remediate → rescan

## Detection & Analysis (Before)
- none

## Detection & Analysis (After)
- Findings: **1 Low — TCP Timestamps Information Disclosure (macOS)**  
  Context: macOS doesn’t expose a supported toggle to disable TCP timestamps; impact is informational (uptime inference).

## Containment / Eradication / Recovery
- Applied macOS hardening: installed OS updates, enabled Firewall, disabled unnecessary Sharing services.
- **Risk Decision:** Accepted for macOS host (no supported control to fully disable timestamps); exposure minimized by limiting services and patching.

## Results (Before → After)
- Before: <counts, if you have them>  
- After: **1 Low (timestamps, accepted)**  
  See `evidence/after_summary.png` and `evidence/timestamps_after.png`.

## Lessons Learned
- DHCP can change host IPs; use DHCP reservation or a small CIDR/range.
- Document OS-specific constraints in remediation plans.
