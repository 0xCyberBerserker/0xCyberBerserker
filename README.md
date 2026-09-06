<div align="center">
  <h1>0xCyberBerserker</h1>
  <p><strong>Cybersecurity Engineer focused on offensive security, reverse engineering, Linux systems, and security automation.</strong></p>
  <p><em>Building security and systems tooling that stays useful when the lab gets noisy.</em></p>
  <p>
    <a href="https://github.com/0xCyberBerserker/spc-glee-a64-linux"><img alt="SPC Glee A64 Linux" src="https://img.shields.io/badge/SPC%20Glee%20A64-Linux%20%2F%20ARM64-0a1324?style=for-the-badge&logo=linux&logoColor=ffcc00&labelColor=07111d"></a>
    <a href="https://github.com/0xCyberBerserker/ghosttrace-lab"><img alt="GhostTrace Lab" src="https://img.shields.io/badge/GhostTrace-malware%20analysis-0a1324?style=for-the-badge&logo=github&logoColor=46f3ff&labelColor=07111d"></a>
    <a href="https://github.com/0xCyberBerserker/OSCP-Arsenal"><img alt="OSCP Arsenal" src="https://img.shields.io/badge/OSCP%20Arsenal-offline%20toolkit-0a1324?style=for-the-badge&logo=kalilinux&logoColor=9fef00&labelColor=07111d"></a>
  </p>
  <p>
    <a href="https://github.com/0xCyberBerserker/aur-incident-defense-kit"><img alt="AUR Incident Defense Kit" src="https://img.shields.io/badge/AUR%20Incident-defense%20kit-0a1324?style=for-the-badge&logo=archlinux&logoColor=1793d1&labelColor=07111d"></a>
    <a href="https://github.com/0xCyberBerserker/codex-ui-linux-port"><img alt="Codex UI Linux Port" src="https://img.shields.io/badge/Codex%20UI-Linux%20packages-0a1324?style=for-the-badge&logo=linux&logoColor=ffcc00&labelColor=07111d"></a>
    <a href="https://github.com/0xCyberBerserker/warpdesk"><img alt="WarpDesk" src="https://img.shields.io/badge/WarpDesk-Qt%20for%20Linux-0a1324?style=for-the-badge&logo=qt&logoColor=41cd52&labelColor=07111d"></a>
  </p>
  <p>
    <a href="https://www.linkedin.com/in/jcarlosgl-offensive-security/">LinkedIn</a>
    · <a href="https://app.hackthebox.com/users/3633924">Hack The Box</a>
    · <a href="#open-source--upstream">Open Source</a>
  </p>
  <p>
    <img alt="Focus" src="https://img.shields.io/badge/focus-security%20engineering-0a1324?style=flat-square&labelColor=07111d&color=46f3ff">
    <img alt="Location" src="https://img.shields.io/badge/Barcelona-Spain-0a1324?style=flat-square&labelColor=07111d&color=ff4fd8">
  </p>
</div>

---

## Engineering focus

I take engineering work from investigation to a reproducible, documented result:
hardware and software evidence, maintainable implementation, CI/release automation,
and operator-facing tooling. I prefer explicit security boundaries, reversible changes,
and debugging claims backed by artifacts or tests. Security work is limited to
authorized environments and defensive research.

---

## Selected engineering

<table>
  <thead>
    <tr>
      <th>Project</th>
      <th>Engineering result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://github.com/0xCyberBerserker/spc-glee-a64-linux">SPC Glee A64 Linux</a></td>
      <td>Brought Linux/ARM64 to an unsupported Allwinner A64 tablet with reproducible U-Boot, TF-A, and kernel tooling. The minimal hardware-tested Device Tree cold-boots from microSD to systemd; the Linux board-support PATCH v1 is submitted for upstream review.</td>
    </tr>
    <tr>
      <td><a href="https://github.com/0xCyberBerserker/ghosttrace-lab">GhostTrace Lab</a></td>
      <td>Reverse-engineering and malware-analysis workbench connecting static and dynamic evidence, Ghidraaas, local/configurable LLM reasoning, a Windows sandbox, x64dbg integration, and persistent triage workflows.</td>
    </tr>
    <tr>
      <td><a href="https://github.com/0xCyberBerserker/OSCP-Arsenal">OSCP Arsenal</a></td>
      <td>Offline-first offensive-security reference with 201 tool sheets and 16 interactive methodology paths, delivered as a PWA and Qt/QML reader with Linux, Windows, and Android builds plus OIDC/Sigstore provenance.</td>
    </tr>
    <tr>
      <td><a href="https://github.com/0xCyberBerserker/aur-incident-defense-kit">AUR Incident Defense Kit</a></td>
      <td>Non-destructive Arch/AUR supply-chain incident auditing that preserves evidence hashes, correlates packages, timelines, IOCs, provenance, and integrity, then produces a remediation plan.</td>
    </tr>
    <tr>
      <td><a href="https://github.com/0xCyberBerserker/codex-ui-linux-port">Codex UI Linux Port</a></td>
      <td>Auditable release automation for Arch/CachyOS, Debian/Ubuntu, and RPM packages, with upstream source tracking, hash verification, GitHub Actions, and an explicit public/private data boundary.</td>
    </tr>
    <tr>
      <td><a href="https://github.com/0xCyberBerserker/warpdesk">WarpDesk</a></td>
      <td>Native-feeling PySide6/Qt frontend for Cloudflare WARP on Linux with profiles, diagnostics, multilingual desktop integration, and a theme-aware system palette.</td>
    </tr>
  </tbody>
</table>

---

## Open Source / Upstream

- **Linux kernel:** submitted the SPC Glee A64 minimal board-support PATCH v1
  for upstream review. The exact candidate DTB was hardware-tested through a
  cold boot to systemd from microSD. [Follow the public review on Lore](https://lore.kernel.org/all/20260906-b4-spc-glee-a64-v1-v1-0-621df2155e31@proton.me/).
- **HKUDS/CLI-Anything:** contributed the PowerShell installer for the Codex
  skill through [PR #55](https://github.com/HKUDS/CLI-Anything/pull/55), merged
  upstream and credited in the [v0.2.0 release](https://github.com/HKUDS/CLI-Anything/releases/tag/v0.2.0).

---

## Other work / Community

- [token-rat-esp](https://github.com/0xCyberBerserker/token-rat-esp) — Spanish Codex skill for compact, maintainable engineering workflows.
- [Santuario Dana](https://github.com/0xCyberBerserker/paginaSantuarioDana) — volunteer software supporting an animal sanctuary affected by the Valencia DANA disaster.
- [Mente Activa](https://github.com/0xCyberBerserker/mente-activa) — accessible educational activities for older adults, families, and caregivers.

---

## Community roots

Former global moderator of two historic Spanish-speaking security communities:

- [Cuadernos de Hack x Crack](https://elhacker.info/manuales/Hacking%20y%20Seguridad%20informatica/Cuadernos%20Hack%20x%20Crack/) — the material that first pulled me toward computing and hacking.
- [Hack x Crack archive](https://web.archive.org/web/20200923003951/https://hackxcrack.net/foro/profile/3hy%21/)
- [Underc0de profile](https://underc0de.org/foro/index.php?action=profile;u=1971)

That background still shapes how I evaluate tools: useful beats decorative,
evidence beats noise, and public work should be clear about its boundaries.

---

## Contact

- GitHub: [github.com/0xCyberBerserker](https://github.com/0xCyberBerserker)
- LinkedIn: [linkedin.com/in/jcarlosgl-offensive-security](https://www.linkedin.com/in/jcarlosgl-offensive-security/)

<div align="center">
  <sub>Barcelona, Spain · Made with 🖤 in Barcelona City 🇪🇸</sub>
</div>
