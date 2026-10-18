# MedXpert — Medical Device Compliance Line — Organization Home

[![Org](https://img.shields.io/badge/MedXpert-Medical%20Device%20Compliance%20AI-blue.svg)](https://github.com/Medxpert-org)
[![Site](https://img.shields.io/badge/site-medxpert.cn-blue.svg)](https://medxpert.cn)

> Medical-device compliance AI tools and knowledge base. Ownership: 赵兴华 / Steven Zhao·China (ORCID [0009-0001-0512-1237](https://orcid.org/0009-0001-0512-1237)) · Site: [medxpert.cn](https://medxpert.cn)

## What this organization hosts

| Category | Repo | Description |
|---|---|---|
| Skill library | [medxpert-skills](https://github.com/Medxpert-org/medxpert-skills) | Medical-device compliance AI skills (NMPA / FDA 510(k) / EU MDR / PMDA), one folder per skill |
| Skill index | [medxpert-skill-index](https://github.com/Medxpert-org/medxpert-skill-index) | Skill catalog & installation guide |
| Theory | [lgd-theory](https://github.com/Medxpert-org/lgd-theory) | LGD full-lifecycle governance doctrine (shared theory base with the SynomosAI line) |

## Panorama

MedXpert (this org, medical-device compliance line) × SynomosAI·LGD (AI governance line, at [zhaoxinghua09-cell](https://github.com/zhaoxinghua09-cell)) form the full matrix of two main lines; topic search: [topic:medxpert](https://github.com/topics/medxpert).

## Quick start

1. Browse the skill library: https://github.com/Medxpert-org/medxpert-skills
2. Skill index & installation guide: https://github.com/Medxpert-org/medxpert-skill-index
3. LGD theory base: https://github.com/Medxpert-org/lgd-theory

```bash
# list organization repositories
gh repo list Medxpert-org --limit 50

# clone the compliance skill library
git clone https://github.com/Medxpert-org/medxpert-skills.git

# topic search across the org
gh search repos --topic medxpert --owner Medxpert-org
```

## Ownership notes

- Executable code is licensed per each repo's LICENSE; **theory texts / methodologies / normative statements reserve all rights**.
- **Brand status**: MedXpert, SynomosAI, LGD — **no entity registration, no trademark registration**.
- Content is compiled from public official information and is not regulatory advice; rely on the latest regulator publications for key data.
- Ownership declaration source: "LGD External Representation Standard" v1.2 §3.2.

---

## LGD Governance Line · Core 5 Entry (source correction)

> **Source correction**: `Medxpert-org/lgd-theory` listed above is an **org-side historical mirror**; the authoritative source of LGD theory lives at **[`zhaoxinghua09-cell/lgd-theory`](https://github.com/zhaoxinghua09-cell/lgd-theory)**. Cite and contribute against the authoritative source.

| Layer | Repo (`owner/repo`) | Description |
|---|---|---|
| Theory | [`zhaoxinghua09-cell/lgd-theory`](https://github.com/zhaoxinghua09-cell/lgd-theory) | LGD full-lifecycle governance doctrine · concept DOI 10.5281/zenodo.22456647 |
| Protocol | [`zhaoxinghua09-cell/uibc-core`](https://github.com/zhaoxinghua09-cell/uibc-core) | Reference implementation + conformance tests (code Apache-2.0) |
| Verification | [`zhaoxinghua09-cell/silent-failure-catalog`](https://github.com/zhaoxinghua09-cell/silent-failure-catalog) · [`zhaoxinghua09-cell/assayance`](https://github.com/zhaoxinghua09-cell/assayance) | Silent-failure catalog · meta-method judging "whether a check is a check" |
| Entry | [`zhaoxinghua09-cell/LGD`](https://github.com/zhaoxinghua09-cell/LGD) | Public entry & contribution system: RUN IT / BREAK IT / BUILD IT |

## Repository structure

- `profile/README.md` — org home page content (same source as this README)
- `README.md` — this repo's description & org overview
- `SECURITY.md` — organization-level security policy
- `CONTRIBUTING.md` — contribution guide
- `CODE_OF_CONDUCT.md` — code of conduct
- `NOTICE.md` — org-level notice
- `PULL_REQUEST_TEMPLATE.md` — PR template
- `.github/workflows/` · `.github/rulesets/` — org-level CI & rules configuration
- `llms.txt` / `llms-full.txt` / `AGENTS.md` / `README.en.md` — AI discoverability files

## License / License notice

This repository is an **organization facade & configuration repo and carries no standalone LICENSE file**. Executable code is licensed per each repo's LICENSE; theory texts / methodologies / normative statements reserve all rights. Confirm the terms with the maintainers before redistributing org documents.

## Security & contributing

- Security: [SECURITY.md](SECURITY.md)
- Contributing: [CONTRIBUTING.md](CONTRIBUTING.md)
- Code of conduct: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

### Ownership declaration (verbatim from "LGD External Representation Standard" v1.4 §3.2)

```
© 2026 赵兴华 / Steven Zhao·China (ORCID 0009-0001-0512-1237). All rights reserved.
Attribution: LGD (Lifecycle Governance Doctrine) — SynomosAI initiative
Name status: "SynomosAI" / "MedXpert" — not a registered legal entity; no trademark registered
Production reference (self-reported): MedXpert — not a certification or endorsement
Code license: this page carries no code; LGD governance-line code repos are Apache-2.0 (see repo LICENSE)
Cite as: no standalone DOI — theory source zhaoxinghua09-cell/lgd-theory · concept DOI 10.5281/zenodo.22456647
```
