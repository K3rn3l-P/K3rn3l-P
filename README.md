### Kernel

Network engineer (Cisco). Infrastructure, servers, private game servers, home automation.

Most of my repositories are private — they're backups and working notes for machines I actually
run. What the work looks like:

- **Forks I keep alive.** Heavy changes on upstream code, parked on their own branch and re-synced
  against upstream every release instead of left to drift: nine sync branches on one C++ codebase,
  each with its own pre-sync backup. The pinned repo below is the public example of it.
- **Hardening after the fact.** Per-IP rate limiting, brute-force protection, PBKDF2 and HMAC
  token auth, HWID, audit logs, server-side integrity checks that survive a patched updater. And
  a privileged SQL CLR assembly moved out of a `TRUSTWORTHY ON` database into a signed, isolated
  one.
- **Reverse engineering.** Solar inverters, LTE band selection, game packet crypto — usually
  because the hardware is fine and the vendor's software isn't.
- **Machines I can rebuild.** Root-less bootstrap for a clean Linux or Windows install, Arch +
  Hyprland dotfiles that restore this desktop exactly, an indexed archive of Proxmox, GPU
  passthrough and NIC fixes.
- **Agentic coding, on rails.** Refine → Plan → Act, model rotation per phase, my own overrides
  on top of upstream skills.

<sub>On stars, followers and the rest: <a href="https://www.antirez.com/news/171">antirez, news/171</a>.</sub>
