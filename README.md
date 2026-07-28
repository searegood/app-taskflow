# app-taskflow

This repo has **no application source code**. It exists to hold the
CloudBees Unify Application-level workflows that orchestrate a release
across `taskflow-db`, `taskflow-backend`, and `taskflow-frontend`:

- `.cloudbees/workflows/deployer.yaml` — given a manifest, calls each
  component's `deploy.yaml` in the right order.
- `.cloudbees/workflows/release-wf.yaml` — the staged release definition
  (DEV → manual approval → STAGING → PROD) that CloudBees Unify's Release
  Orchestration UI drives.

See [docs/03-multi-component-app.md](../../docs/03-multi-component-app.md)
and [docs/04-release-orchestration.md](../../docs/04-release-orchestration.md).
