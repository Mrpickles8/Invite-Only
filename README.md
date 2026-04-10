# Invite-Only

## Objective
Pivot across IOCs (hash + IP) using VirusTotal to map a full AsyncRAT
attack chain — from execution parents and dropped files to ClickFix phishing
and Discord-based delivery.

### Skills Learned
- SHA256 hash and IP threat intelligence lookup
- IOC pivoting: hash → filename → execution parents → dropped files
- Execution lineage reconstruction (361GJX7J → installer.exe)
- Dropped file identification (Aclient.exe, searchhost.exe, syshelpers.exe,
  nat.vbs, runsys.vbs)
- AsyncRAT malware family identification
- ClickFix phishing technique identification
- Discord-based delivery platform analysis

### Tools Used
- TryDetectThis2.0 (VirusTotal)
- OSINT (external threat intelligence reports)

## Steps
SHA256 hash submitted → filename and file type identified. Execution lineage
revealed two parents: `361GJX7J` then `installer.exe`. installer.exe dropped
`Aclient.exe`. Second parent dropped `searchhost.exe`, `syshelpers.exe`,
`nat.vbs`, `runsys.vbs`. IP `101[.]99[.]76[.]120` confirmed C2 infrastructure.
OSINT correlated findings with AsyncRAT campaign — ClickFix social engineering
via hijacked Discord invites, fake "Safeguard" bot triggering malware download.

*Ref 1: VirusTotal — execution parents and dropped file chain*
*Ref 2: OSINT correlation — AsyncRAT + ClickFix + Discord delivery*
