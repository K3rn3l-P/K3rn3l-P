### Kernel

Network engineer (Cisco). Networks, servers, private game servers, home automation.

Most of my repositories are private and will stay that way, so the public list is a thin
slice. Briefly, what the work actually is:

**Forks that don't rot.** Most of what I run is upstream code with substantial changes on top.
Those changes live on dedicated branches and get re-synced against upstream on a versioned
cadence instead of drifting apart — nine sync branches on one C++ codebase, tagged releases on
another. [anern-eco6200-eybond](https://github.com/K3rn3l-P/anern-eco6200-eybond) is the public
example of the pattern: a Home Assistant integration for Anern ECO-6200 inverters, maintained
over upstream with frame validation, anomaly tracking and stale-data detection.

**Server-side hardening.** Moving a privileged SQL CLR assembly out of a trusted database and
into an isolated one: signature-based authorisation instead of trust flags, wrapper procedures,
a command allowlist with destructive commands disabled by default, least-privilege service
accounts, full audit trail.

**Protocol reverse engineering.** Solar inverters over Modbus and raw TCP, LTE modem band
selection, game client/server packet encryption. Usually because the vendor app is bad and the
hardware is fine.

**Reproducible machines, not hand-tuned boxes.** Bootstrap scripts that take a clean Linux or
Windows install to a working environment at user scope, without root. Disaster-recovery runbooks
that keep versioned config strictly separate from runtime secrets. An indexed archive of
Proxmox, GPU-passthrough and NIC fixes, so I solve them once and not twice.

**A full private-server stack.** C++ core and patching framework, C# control console and
launcher/updater, PHP site, anti-cheat, packet crypto, SQL Server automation.

Daily driver: Arch Linux and Hyprland. Home Assistant runs the house.

<sub>On stars, followers and the rest: <a href="https://www.antirez.com/news/171">antirez, news/171</a>.</sub>
