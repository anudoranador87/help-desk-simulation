# HD-1 — Unable to access websites (DNS misconfiguration)

| Field | Value |
|---|---|
| ID | HD-1 |
| Type | Incident |
| Priority | Medium |
| Jira status in last recorded snapshot | Open — confirm/close separately in Jira |
| Portfolio case status | Completed |
| Requester | Maria Garcia (Finance, fictional) |
| Workstation | WIN11-USER01 |
| Detailed lab and evidence | [IT Support Labs — HD-1 DNS case](https://github.com/anudoranador87/it-support-labs/tree/master/labs/01-dns-misconfiguration) |
| Jira issue | https://fabrikamitsupport.atlassian.net/browse/HD-1 |

## Summary

The simulated Windows 11 workstation could not open websites because its configured DNS resolver (\`192.0.2.1\`) did not answer DNS queries. The incident was investigated by separating IP connectivity from name resolution. The DNS setting was restored to \`8.8.8.8\`, the DNS cache was flushed, and name resolution and browser access were checked again.

## Investigation performed

- Confirmed IP connectivity with \`ping 1.1.1.1\` (4/4 replies).
- Compared baseline DNS resolution using \`nslookup example.com\`.
- Introduced the fault by setting the preferred DNS server to \`192.0.2.1\`.
- Observed repeated \`nslookup\` timeouts against \`192.0.2.1\`.
- Confirmed that the browser could not load websites while the DNS fault was active.
- Kept unrelated observations separate from the confirmed incident cause.

## Root cause

The workstation was configured to use DNS server \`192.0.2.1\`, which did not respond to DNS queries.

## Resolution

From an elevated Command Prompt:

\`\`\`cmd
netsh interface ipv4 set dnsservers name="Ethernet" static 8.8.8.8 primary
ipconfig /flushdns
\`\`\`

The workstation IP address and gateway were not changed.

## Verification

- \`nslookup example.com\` resolved again through \`dns.google\` (\`8.8.8.8\`).
- Microsoft Edge loaded \`https://www.google.com\` after the DNS correction.
- The detailed lab records the checks, screenshots and evidence limitations.

## Evidence

See the [HD-1 evidence and full troubleshooting walkthrough](https://github.com/anudoranador87/it-support-labs/tree/master/labs/01-dns-misconfiguration), including baseline connectivity, DNS fault output, browser failure and recovery.

## Limitations and follow-up

- The detailed lab notes that \`ipconfig /all\` was not captured while the fault was active; the active resolver is visible in the \`nslookup\` output.
- The post-fix \`nslookup\` output was not saved as a screenshot.
- A separate \`curl.exe\` connection-reset observation and the presence of two default gateways were not attributed to this DNS incident.
- The practical case study is completed. The Jira issue was marked **Open** in the last repository snapshot; verify its live state and close it in Jira if it is still open.

## Related planned scenarios

HD-002 through HD-006 remain planned. They must not be presented as completed until they have been performed, verified and documented.
