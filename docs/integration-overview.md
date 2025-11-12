# Integration Overview

## Edge/CDN/WAF
- Deploy allow/deny rules using Live IP Blocklist.
- Cache TTL: short (minutes) for freshness.
- Fallback: soft-fail open on network errors to avoid blocking legit traffic.

## Server Middleware
- For each inbound request, query IP Risk API and attach risk score + flags.
- Example decision: `deny if high_risk or (datacenter && no-human-signal)`.

## Ad Tech (DSP/SSP)
- Pre-bid: suppress impressions/clicks from high-risk IPs.
- Post-bid: reconcile logs to quantify IVT reduction and savings.

## Reporting
- Track filtered traffic, lift in CTR/conv quality, and reduced refund/chargeback rates.
