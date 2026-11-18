# MOSIP AI Toolkit

The central, governed source of reusable AI engineering assets for AI-assisted software development across the MOSIP ecosystem. These assets are skills, prompts, engineering standards and templates.

AI coding assistants such as GitHub Copilot, Claude Code and OpenAI Codex are increasingly used to design, develop, test, review and maintain MOSIP software. This repository keeps approved engineering knowledge in one place, so developers and supported AI tools get the same guidance on MOSIP architecture principles, coding conventions and security requirements. Without it, the same instructions get copied into individual repositories and drift apart.

Reference: [MOSIP AI Developer Hub](https://mosip.atlassian.net/wiki/spaces/KnowledgeBase/pages/2789965830/MOSIP+AI+Developer+Hub)

## Objectives

- Provide one central repository for reusable AI engineering assets.
- Remove duplicated common instructions from individual repositories.
- Make approved assets available to developers and supported AI coding tools.
- Standardise AI-assisted requirements analysis, architecture, development, testing, code review and documentation.
- Encode MOSIP engineering practices, architecture principles and security requirements.
- Stay vendor-neutral, so assets can be reused across MOSIP products and different AI coding assistants.
- Apply governance, versioning and quality assurance to every asset.

## Repository layout

| Area | Purpose |
|---|---|
| [`skills/`](skills/) | Structured instructions that give AI agents the methodology for a specific engineering activity. Each skill follows the open [Agent Skills](https://agentskills.io) specification (`SKILL.md` plus supporting references where required). |
| [`prompts/`](prompts/) | Reusable prompts for specific engineering tasks. Prompts reference skills and standards rather than duplicating them. |
| [`standards/`](standards/) | Authoritative MOSIP engineering standards: architecture principles, coding conventions, API and database design, security baseline, testing and quality. |
| [`templates/`](templates/) | Templates for consistent engineering artefacts: requirement specs, technical designs, ADRs, test plans, review checklists, security assessments, release notes. |

```
mosip-ai-toolkit/
├── README.md
├── VERSION
├── skills/
│   ├── requirements/
│   ├── architecture/
│   ├── development/
│   ├── code-review/
│   ├── testing/
│   ├── security/
│   ├── devops/
│   └── documentation/
├── prompts/
│   ├── requirements/
│   ├── architecture/
│   ├── development/
│   ├── code-review/
│   ├── testing/
│   └── security/
├── standards/
│   ├── architecture/
│   ├── coding/
│   ├── security/
│   ├── database/
│   ├── api/
│   └── testing/
└── templates/
```

## Using the assets

- **Skills:** copy or symlink a skill folder into the location your AI tool reads skills from (for example `.claude/skills/` for Claude Code, or `.github/skills/` or `.agents/skills/` for other Agent Skills-compatible tools). You can also point the tool at this repository.
- **Prompts:** use them as-is, or as the basis for repository-level instruction files.
- **Standards and templates:** reference them from skills, prompts, pull request reviews and design documents.

Pin to a released version (see [`VERSION`](VERSION) and repository tags) instead of tracking a moving branch.

## Branches

| Branch | Purpose |
|---|---|
| `develop` | Integration branch. Open pull requests against `develop`. |
| `master` | Released, approved assets. |

## Governance

MOSIP Engineering owns this repository and coordinates its maintenance.

| Role | Responsibility |
|---|---|
| MOSIP Engineering | Overall ownership and governance |
| Architects | Validation of architecture, design and coding skills |
| Security Team | Security-related skills and standards |
| QA Team | Testing and quality-related skills |
| Product Technical Leads | Product-specific knowledge and validation |
| Contributors | Skill creation, improvements and feedback |

- Every change goes through a pull request and technical review before it is approved.
- Security-related instructions also go through security review.
- Never commit credentials, secrets or sensitive production information.
- Skills guide AI agents. They do not replace mandatory controls such as CI security scans, testing, code review and release approvals.

## Contributing

1. Fork the repository and branch from `develop`.
2. Add or update an asset in the matching area, following the conventions in that folder's `README.md`.
3. Open a pull request against `develop` that links the related issue.

## License

This project is licensed under the [Mozilla Public License 2.0](LICENSE).
