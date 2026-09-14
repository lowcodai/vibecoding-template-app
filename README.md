# itshaker-template-app

> Template for web applications, APIs, MVPs, portals, SaaS products, or internal tools.

[![Governance](https://img.shields.io/badge/governance-lowcodai-blue)](https://github.com/lowcodai/itshaker-copilot-governance)

## Description

GitHub template for itshaker applications and APIs. Includes everything from
`itshaker-template-base`, plus:
- `src/`, `tests/`, `public/` structure
- Accessibility instructions (WCAG 2.1 AA)
- Docker and CI/CD instructions
- Workflows: CI, automated release, a11y-check
- `dependency-license-checker` hook

## Usage

```bash
cd itshaker-bootstrap
./scripts/new-project.sh --type app --name <my-app>
```

## App-specific structure

```
.
├── src/      # Main source code
├── tests/    # Unit, integration, e2e tests
└── public/   # Public static assets
```

## Conventions

- **Accessibility**: WCAG 2.1 AA minimum. Checked via `a11y-check.yml`.
- **Tests**: coverage ≥ 80%. No merge without passing tests.
- **API**: OpenAPI/Swagger spec required for every REST API.
- **Docker**: `Dockerfile` with a minimal image, multi-stage build recommended.

## App-specific Awesome Copilot elements

| Element | Type | Usage |
|---------|------|-------|
| `a11y.instructions.md` | Instruction | Accessibility standards |
| `containerization-docker-best-practices.instructions.md` | Instruction | Docker |
| `dependency-license-checker` | Hook | Licenses |
| `fix-broken-links` | Hook | Broken links in docs |
| `accessibility` | Agent | Accessibility expert |
| `accessibility-runtime-tester` | Agent | Runtime accessibility testing |

See `.github/copilot-instructions.md` for this repo's full active hooks list, and the [governance hooks registry](https://github.com/lowcodai/itshaker-copilot-governance/blob/main/docs/awesome-copilot-map.md) for the full ecosystem-wide catalog.

## References

- [itshaker-copilot-governance](https://github.com/lowcodai/itshaker-copilot-governance)
- [WCAG 2.1](https://www.w3.org/TR/WCAG21/)
