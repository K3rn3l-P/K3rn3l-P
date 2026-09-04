### Kernel

I'm a network engineer (Cisco). Most days that means infrastructure — networks, servers,
virtualisation — and a fair amount of code that has to keep running when nobody is watching it.

Nearly everything I write lives in private repositories. That's not secrecy so much as the fact
that most of them are backups and working notes for machines I actually run. It does mean this
profile looks emptier than the work is, so here's a summary of it instead.

#### Forks I actually maintain

I run a lot of upstream code with heavy changes on top. Rather than let a fork drift until it
can't be merged again, I keep my own work on its own branch and re-sync against upstream every
time upstream ships — one branch per version. One C++ codebase is at nine of those by now
(`modifiche-sync-main-v0.9` through `v1.3s`), each with a pre-sync backup branch, because I have
lost custom hooks in a merge before and had to go dig them back out.

The one you can actually look at is
[anern-eco6200-eybond](https://github.com/K3rn3l-P/anern-eco6200-eybond), a Home Assistant
integration for Anern ECO-6200 inverters that talks to an EyBond Wi-Fi dongle over reverse-TCP
and Modbus. Upstream targets different hardware, so my side adds frame validation, anomaly
counting and stale-versus-fresh detection. The failures used to be silent, which is the worst
kind to debug.

#### Security work

Mostly the kind that comes after something already works. On the game-server stack: per-IP and
per-connection rate limiting, brute-force protection on login, single-use login nonces, PBKDF2
and HMAC-SHA256 token auth, HWID checks, an audit log, server-side binary integrity checks that
still hold if someone patches the updater, and AES-256-GCM on the client data archive.

Separately, moving a privileged SQL CLR assembly out of a database running `TRUSTWORTHY ON` and
into an isolated one, authorised by signature instead of by trust flag — wrapper procedures, a
command allowlist with the destructive entries disabled by default, least-privilege accounts,
and every command logged.

#### Reverse engineering

Solar inverters, LTE modem band selection, game client and server packet encryption. Usually
because the hardware is fine and the vendor's software isn't.

#### Machines I can rebuild

Bootstrap scripts that take a clean Linux or Windows install to a working environment at user
scope, without root. Dotfiles that restore this Arch + Hyprland desktop exactly, including the
step that reminds me to check the LUKS passphrase is still typeable on the new keyboard layout
*before* rebooting. And an indexed archive of Proxmox, GPU-passthrough and NIC fixes, so nothing
has to be worked out twice.

<sub>On stars, followers and the rest: <a href="https://www.antirez.com/news/171">antirez, news/171</a>.</sub>
