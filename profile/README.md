<div align="center">
  <img src="https://raw.githubusercontent.com/technical-turtle/.github/main/profile/logo.png" alt="Technical Turtle" width="84" />
  <h1>Technical Turtle</h1>
  <p><strong>Developer tools and engineering for distributed systems, cloud, and AI-native software.</strong></p>
</div>

---

I design, architect, and build software.<br>
Distributed systems, cloud platforms, full-stack applications, cyber security, AI tooling, and more. 18+ years crafting complex systems at ASML, Philips, and Ibeo, with a Professional Doctorate in Engineering and an AWS Solutions Architect Professional certification.

## Postgres Migration Safety Auditor

Catch the database migration that locks or rewrites your production table, before it reaches production.

```sql
-- looks fine in review, locks your busiest table in prod:
ALTER TABLE users ALTER COLUMN email SET NOT NULL;

-- the safe rewrite the auditor points you to:
ADD CONSTRAINT c CHECK (email IS NOT NULL) NOT VALID;  VALIDATE CONSTRAINT c;  then SET NOT NULL;
```

A static auditor for Flyway and Liquibase that flags each production hazard with the reason and the safe rewrite. It parses your migration with the real PostgreSQL parser, cites an official source for every rule, and runs as a CLI, a CI gate, or a Claude Code skill. It never connects to your database. One-time, EUR 14.99.

**[Product page and free migration cheatsheet](https://technical-turtle.com/postgres-migration-auditor)**

## Free and open source

- **Postgres Migration Guard** (`pg-migration-guard`) - the free version of the auditor: the ten common Postgres migration hazards, as a CLI and a GitHub Action. [Repository](https://github.com/technical-turtle/pg-migration-guard)
- **Claude Code Context Telemetry** (`cc-context-telemetry`) - see your Claude Code context and usage limits in your statusline, and read them from your hooks. [Repository](https://github.com/technical-turtle/cc-context-telemetry)

## Elsewhere

- Website and storefront (full product list): **[technical-turtle.com](https://technical-turtle.com)**
- Contact: hello@technical-turtle.com
