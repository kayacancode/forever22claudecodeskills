# Forever22 Claude Code Skills

Security and productivity skills for Claude Code by [Forever22 Studios](https://forever22studios.com).

## Install

```bash
/plugin marketplace add kayacancode/forever22claudecodeskills
```

## Skills

### /pentest

ReAct-style web penetration testing for authorized targets. Runs a 5-phase pipeline inspired by recent arxiv research (PentestAgent, RapidPen, Excalibur):

1. **Recon** — DNS, headers, port scan, TLS, WAF detection
2. **Discovery** — path fuzzing, API enumeration, tech fingerprinting
3. **Vuln Scan** — nuclei, CORS, cookies, HTTP methods, version disclosure
4. **Deep Probe** — targeted tests based on findings (auth bypass, IDOR, XSS, SQLi, SSTI)
5. **Report** — structured markdown with OWASP categories, severity ratings, evidence, remediation

```bash
/pentest https://target.com --scope web
/pentest https://api.target.com --scope api --auth-header "Authorization: Bearer ..."
```

**Requires:** `curl`, `dig` (built-in). **Recommended:** `nmap`, `ffuf`, `nuclei`.

```bash
brew install nmap ffuf nuclei
```

## Requirements

- Claude Code v2.1+
- macOS or Linux
- Authorization to test the target (mandatory)

## License

MIT
