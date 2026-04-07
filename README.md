# Invite-Only

## Objective
Analyze a suspicious email invitation to identify embedded malicious content, trace the delivery mechanism, and document the indicators of compromise associated with the phishing attempt.

### Skills Learned
- Malicious email artifact analysis
- Embedded link and attachment investigation
- Sandbox detonation and behavioral analysis
- IOC identification and threat reporting

### Tools Used
- Email client and header analyzer
- VirusTotal and URLScan.io
- Sandboxed browser environment
- Text editor for raw email source inspection

## Steps
The investigation started with extracting the raw email source to examine headers and identify the sending infrastructure. Embedded links were defanged and submitted to URLScan.io for passive analysis. Attachments were detonated in a sandboxed environment to observe behavioral indicators. All IOCs were compiled into a structured report including sender IP, malicious domains, and file hashes.

*Ref 1: Raw email source with embedded malicious URL identified*
*Ref 2: URLScan.io analysis of the destination phishing page*
