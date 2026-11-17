## Sabri L.

**Detection engineering · Threat analysis · Security tooling**

I build tools that test whether security controls actually hold, and the data pipelines needed to
back those answers with evidence. My work is measured, reproducible and documented down to its limits.

MSc in Computer Science (MIAGE), Cybersecurity track, Université de Haute-Alsace, France.

---

### Selected work

**[sigma-mutate](https://github.com/zabubu/sigma-mutate)** · Evasion testing for detection rules  
Rewrites attack command lines into forms Windows treats as identical (quote insertion, whitespace,
alternate flags) and checks whether [Sigma](https://github.com/SigmaHQ/sigma) rules still fire.
Across 1,193 public process-creation rules, **97% of those with a conclusive result miss at least one
equivalent variant**. All 193 default rewrites were executed on a real Windows host, and the engine's
22,002 verdicts were cross-checked against an independent implementation with zero disagreement.  
<sub>Python · Sigma · Windows internals · Detection engineering</sub>

**[honeypot-map](https://github.com/zabubu/honeypot-map)** · SSH honeypot and attack analysis pipeline  
Internet-exposed Cowrie honeypot feeding an ingestion and GeoIP/ASN enrichment pipeline, a REST and
WebSocket API, a live attack map and an automated analysis report. First collection: 6,845 SSH
sessions from 97 addresses in 21 hours, with identical wordlists traced across coordinated hosts.  
<sub>Python · Cowrie · FastAPI · WebSocket · SQLite · Docker · Leaflet</sub>

**[txray](https://github.com/zabubu/txray)** · Pre-signing risk analysis for EVM transactions  
Decodes what a wallet is about to sign (transactions, EIP-712 permits and Seaport orders, SIWE
messages) and returns an explained `pass` / `warn` / `block` verdict. Includes a bytecode
disassembler and control-flow analysis, proxy resolution and an authenticated, rate-limited API.
191 tests, 90% line and branch coverage.  
<sub>Python · EVM · EIP-712 · Static analysis · FastAPI</sub>

**[costlake](https://github.com/zabubu/costlake)** · Lakehouse for cloud billing data  
Ingests FOCUS billing exports from AWS, Azure and Google Cloud into a bronze/silver/gold lake on S3,
with a blocking quality gate, quarantine, idempotent restatement handling, anomaly detection and
alerting. Infrastructure defined in Terraform and tested offline; integration tests run the full
pipeline end to end.  
<sub>Python · Polars · DuckDB · dbt · Dagster · PostgreSQL · Terraform · Prometheus · Grafana</sub>

---

### Open source

- **[SigmaHQ/sigma#6562](https://github.com/SigmaHQ/sigma/pull/6562)** (merged): fixed a rule that
  could never fire on Windows logs because of an incorrect path separator. Found with sigma-mutate.

---

### Technical scope

| Area | |
|---|---|
| Security | Detection engineering (Sigma), honeypots (Cowrie), log analysis, Linux server hardening, EVM bytecode and signature analysis |
| Languages | Python, TypeScript, SQL, C++, PHP |
| Backend and data | FastAPI, WebSocket, PostgreSQL, SQLite, Polars, DuckDB, dbt, Dagster |
| Infrastructure | Linux, Docker Compose, Terraform, AWS (S3, IAM), GitHub Actions |
| Observability | Prometheus, Loki, Grafana |

---

### How I work

- **Measure before claiming.** Results come with their method, their sample size and their limits.
- **Verify independently.** Critical outputs are cross-checked against a second implementation or a real system.
- **Ship it reproducible.** Every project runs from a clean clone and ships with automated tests.
