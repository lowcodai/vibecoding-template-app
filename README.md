# itshaker-template-app

> Template pour applications web, API, MVP, portail, SaaS ou outil interne.

[![Governance](https://img.shields.io/badge/governance-itshaker-blue)](https://github.com/itshaker/itshaker-copilot-governance)

## Description

Template GitHub pour applications et APIs itshaker. Inclut tout `itshaker-template-base` plus :
- Structure `src/`, `tests/`, `public/`
- Instructions accessibilité (WCAG 2.1 AA)
- Instructions Docker et CI/CD
- Workflows : CI, release automatisée, a11y-check
- Hook `dependency-license-checker`

## Utilisation

```bash
cd itshaker-bootstrap
./scripts/new-project.sh --type app --name <mon-app>
```

## Structure spécifique app

```
.
├── src/      # Code source principal
├── tests/    # Tests unitaires, intégration, e2e
└── public/   # Assets statiques publics
```

## Conventions

- **Accessibilité** : WCAG 2.1 AA minimum. Vérification via `a11y-check.yml`.
- **Tests** : coverage ≥ 80%. Pas de merge sans tests verts.
- **API** : OpenAPI/Swagger spec obligatoire pour toute API REST.
- **Docker** : `Dockerfile` avec image minimale, build multi-stage recommandé.

## Éléments Awesome Copilot spécifiques

| Élément | Type | Usage |
|---------|------|-------|
| `a11y.instructions.md` | Instruction | Standards accessibilité |
| `containerization-docker-best-practices.instructions.md` | Instruction | Docker |
| `dependency-license-checker` | Hook | Licences |
| `fix-broken-links` | Hook | Liens brisés dans la doc |
| `accessibility` | Agent | Expert accessibilité |
| `accessibility-runtime-tester` | Agent | Tests accessibilité runtime |

## Références

- [itshaker-copilot-governance](https://github.com/itshaker/itshaker-copilot-governance)
- [WCAG 2.1](https://www.w3.org/TR/WCAG21/)
