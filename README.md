### Kernel

Most of my repositories are private — they're backups and working notes for machines I actually
run. What the work looks like:

- **Networks.** pfSense and OPNsense edges, Catalyst from the serial console, Ubiquiti
  point-to-point radio links, UniFi gateways. VLAN segmentation with zone-based firewalling,
  policy routing to per-segment VPN egress, 802.1X port profiles over RADIUS, scoped multicast
  reflection, split-horizon DNS behind a single reverse proxy, WAF and identity-aware access at
  the edge, DNS-01 certificates so internal hostnames carry real TLS.
- **Forks I keep alive.** Heavy changes on upstream code, parked on their own branch and re-synced
  against upstream every release instead of left to drift: a C++ codebase running tens of
  thousands of lines ahead of upstream across dozens of files, each sync with its own pre-sync
  backup. The pinned Home Assistant integration below is the public sample of it.
- **Hardening after the fact.** Per-IP rate limiting, brute-force protection, PBKDF2 and HMAC
  token auth with constant-time verification and a versioned hash scheme that migrates in place,
  HWID, structured audit logs, server-side integrity checks that survive a patched updater.
  Scheduled key rotation with payload re-encryption and session invalidation. And a privileged
  SQL CLR assembly moved out of a `TRUSTWORTHY ON` database into a signed, isolated one, reached
  only through wrappers that deny by default — migrated in stages on a live system, with rollback
  and a verification pass that tests the denials, not just the happy path.
- **Reverse engineering.** Serial and Modbus device protocols, down to undocumented registers
  when the documented command silently fails, with strict CRC and frame-integrity handling.
  Radio and mobile APIs: band masks, carrier aggregation, cell identity decoding. Encrypted
  asset archives, packet crypto, anti-tamper and integrity checks, tooling injected into closed
  binaries, assembly hooks and memory injection — usually because the hardware is fine and the
  vendor's software isn't.
- **Machines I can rebuild.** Root-less, package-manager-agnostic bootstrap for a clean Linux or
  Windows install. Idempotent installers with backup on overwrite, privilege separation between
  user-scope and system steps, pre-reboot verification of full-disk-encryption unlock. Unattended
  Windows VM provisioning.
- **Agentic coding, on rails.** Refine → Plan → Act, model rotation per phase, my own overrides
  on top of upstream skills. And guardrails in code rather than in the prompt for an agent acting
  on a live server: tiered actions, deny-by-default allowlists with an independent second check,
  a file kill-switch, read-only credentials by default, and mandatory human approval for anything
  irreversible.
- **Languages.** C++, C, Assembly, C#, Java, Python, JavaScript, TypeScript, PHP, Lua, Shell,
  PowerShell, TSQL, HLSL, QML, Liquid.

<sub>On stars, followers and the rest: <a href="https://www.antirez.com/news/171">antirez, news/171</a>.</sub>
