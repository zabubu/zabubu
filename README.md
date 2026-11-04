### Hi, I'm Sabri 👋

Cybersecurity graduate with a **Master's degree in MIAGE** (*Méthodes Informatiques Appliquées à la
Gestion des Entreprises*), **Cybersecurity track**, from the Université de Haute-Alsace in Mulhouse, France.

I'm drawn to the defensive side of security: **detection engineering**, **threat analysis** and
understanding what attackers actually do once they get in.

---

### 🔬 Featured projects

**[sigma-mutate](https://github.com/zabubu/sigma-mutate)**: a crash test for detection rules.
It rewrites attack commands in ways that change nothing for Windows (extra quotes, spaces, alternate
flags) and checks whether [Sigma](https://github.com/SigmaHQ/sigma) rules still fire.
Run against 1,193 public rules: **97% of the testable ones can be evaded** this way. Every rewrite was
validated on a real Windows machine.
`Python` `Sigma` `Windows` `Detection engineering`

**[honeypot-map](https://github.com/zabubu/honeypot-map)**: an SSH honeypot exposed to the Internet,
with a full pipeline behind it. Cowrie captures the bots, Python ingests and enriches each attack with
GeoIP data, and a live dashboard draws the attacks on an animated world map. It also generates an
automatic analysis report.
`Cowrie` `Python` `FastAPI` `WebSocket` `SQLite` `Docker` `Leaflet`

---

### 🤝 Open source

- [SigmaHQ/sigma#6562](https://github.com/SigmaHQ/sigma/pull/6562): fix for a Sigma rule
  (*COM Object Execution via Xwizard.EXE*) that could never fire on Windows logs because of a
  wrong path separator. Found with sigma-mutate.

---

### 🛠️ Tools & technologies

**Security:** Sigma · Cowrie · log analysis · server hardening
**Languages:** Python · C++ · PHP · SQL
**Tooling:** Docker · FastAPI · Git · GitHub Actions · Linux
