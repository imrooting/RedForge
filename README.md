# 🔴 RedForge CommandKit

> A browser-based command generator for internal penetration testing. Fill in your credentials and targets once — get correctly formatted tool commands instantly.

---

## What It Does

RedForge takes your engagement credentials (username, password, hash, domain, IPs) and generates ready-to-run commands for common pentest tools — no more typos, no more forgetting flags.

All commands are verified against official tool documentation. Works completely offline with no network requests, making it safe on air-gapped lab machines.

---

## Supported Tools

### Linux / Cross-Platform
- **Impacket** — secretsdump, psexec, wmiexec, smbclient, GetUserSPNs, GetNPUsers, getTGT, getST, ticketer, addcomputer
- **NetExec (nxc)** — SMB enumeration, remote exec, password spray, LDAP queries, WinRM, coercion
- **Certipy** — AD CS enumeration, certificate request, authentication, shadow credentials, relay attacks
- **bloodyAD** — RBCD, GenericAll/Write, password reset, group membership, shadow credentials, DCSync
- **Misc** — ntlmrelayx, responder, john/hashcat cracking, ligolo-ng tunneling

### Windows
- **Rubeus** — AS-REP roasting, Kerberoasting, PTT, PTH, S4U, ticket harvesting, Golden/Silver tickets
- **Mimikatz** — sekurlsa, lsadump, token impersonation, DCSync, Pass-the-Hash
- **PowerView / RSAT** — AD enumeration, ACL inspection, BloodHound ingestion
- **Living off the land** — certutil, reg, schtasks, sc (persistence)

---

## How to Use

1. Open `https://imrooting.github.io/RedForge/index.html` in any modern browser
2. Fill in your credentials and targets in the top panel (username, password/hash, domain, DC IP, target, LHOST/LPORT)
3. Select a tool from the left sidebar
4. Pick a module/attack type
5. Set any extra options that appear
6. Click **Generate Command** and copy

> **Credential priority:** AES256 key → NT Hash → Password. The tool automatically picks the strongest credential available for each command.

---

## Features

- **Fully offline** — zero network requests, safe on isolated lab networks
- **Auto credential selection** — picks AES key over hash over password automatically
- **Per-command tips** — each generated command includes an inline usage note
- **Linux + Windows tabs** — separate views for each attack platform
- **Copy to clipboard** — one click to copy the generated command
- **No install needed** — single self-contained HTML file

---

## Requirements

Just a modern browser (Chrome, Firefox, Edge). No server, no dependencies, no internet.

---

## Tested Tool Versions

| Tool | Version |
|---|---|
| impacket | v0.14 |
| certipy | v5 |
| NetExec (nxc) | latest |
| bloodyAD | v2.x |
| Rubeus | v2.3.3 |

---

## ⚠️ Disclaimer

RedForge is intended for **authorized penetration testing and security research only**. Use only on systems and networks you have explicit written permission to test. Misuse of this tool may violate laws and regulations.
