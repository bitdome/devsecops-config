# DevSecOps Config – Documentazione Interna

## Scopo del repository
Centralizza configurazioni di sicurezza, qualità e analisi dei progetti Node.js e Flutter.

## Componenti presenti
- Semgrep (SAST)
- ESLint Security (Node.js)
- Dart Code Metrics (Flutter)
- Snyk (dipendenze)
- GitHub Actions workflow riutilizzabile
- GitLab CI pipeline

## Struttura del repository
```
devsecops-config/
  .github/workflows/security-analysis.yml
  semgrep/
  eslint/
  dart/
  snyk/
  README.md
  DOCUMENTAZIONE_INTERNA.md
```
## Uso nei repository GitHub
```
name: Security Analysis
on: [push, pull_request]
jobs:
  devsecops:
    uses: YOURORG/devsecops-config/.github/workflows/security-analysis.yml@main
```
## Uso nei repository GitLab
```
include:
  - project: 'YOURORG/devsecops-config'
    file: '/.gitlab-ci.yml'
```
## Sicurezza & Robustezza
- Analisi statica: Semgrep, CodeQL, ESLint
- Dipendenze: Snyk
- Test automatici: Node.js + Flutter
- Code Metrics: Dart Code Metrics
