<div align="center">
  <img src="https://raw.githubusercontent.com/technical-turtle/.github/main/profile/logo.png" alt="Technical Turtle" width="84" />
  <h1>Technical Turtle</h1>
  <p><strong>Developer tools and engineering for distributed systems, cloud, and AI-native software.</strong></p>
</div>

---

Focused developer tools that each solve a real production problem, built and maintained by an experienced full-stack engineer. Everything here is meant to run in a real pipeline, not a demo.

## Products

### Postgres Migration Safety Auditor

Catch the database migration that locks or rewrites your production table, before it ships.

```sql
-- ships fine in review, locks your busiest table in prod:
ALTER TABLE users ALTER COLUMN email SET NOT NULL;

-- the safe rewrite the auditor points you to:
ADD CONSTRAINT c CHECK (email IS NOT NULL) NOT VALID;  VALIDATE CONSTRAINT c;  then SET NOT NULL;
```

A static auditor for Flyway and Liquibase that flags each production hazard with the reason and the safe rewrite. It parses your migration with the real PostgreSQL parser, cites an official source for every rule, and runs as a CLI, a CI gate, or a Claude Code skill. It never connects to your database.

One-time, EUR 14.99. **[Product page and free migration cheatsheet](https://technical-turtle.com/postgres-migration-auditor)**

### cc-context-telemetry

[![npm](https://img.shields.io/npm/v/cc-context-telemetry)](https://www.npmjs.com/package/cc-context-telemetry) [![license](https://img.shields.io/npm/l/cc-context-telemetry)](https://github.com/technical-turtle/cc-context-telemetry/blob/main/LICENSE)

Show Claude Code's context % and Pro/Max usage limits, each with a reset countdown, right in your statusline, and bridge them to your hooks and plugins.

```
before:  ~/code/myapp  main
after:   ctx 48% | 5h 14% ~1h20m | 7d 21% ~5d10h | opus-4.8   ~/code/myapp  main
```

```bash
npm i -g cc-context-telemetry
```

Free and MIT. **[Repository and docs](https://github.com/technical-turtle/cc-context-telemetry)**

## Elsewhere

- Website and storefront: **[technical-turtle.com](https://technical-turtle.com)**
- Contact: hello@technical-turtle.com
