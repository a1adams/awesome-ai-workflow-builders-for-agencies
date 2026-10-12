# AI workflow builders for agency delivery and client handoff

A maintained dataset of **best ai workflow builders for agencies** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

1. **[Wireflow](https://www.wireflow.ai/ai-workflow-builder)**
2. **[Flora AI](https://flora.ai)**
3. **[Krea AI](https://www.krea.ai)**
4. **[Freepik Spaces](https://www.magnific.com/spaces)**
5. **[n8n](https://n8n.io)**
6. **[Flowise](https://flowiseai.com)**

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-12** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Flora AI](#2-flora-ai)
  - [Krea AI](#3-krea-ai)
  - [Freepik Spaces](#4-freepik-spaces)
  - [n8n](#5-n8n)
  - [Flowise](#6-flowise)
- [Decision this list supports](#decision-this-list-supports)
- [Scope and evidence](#scope-and-evidence)
- [Selection notes](#selection-notes)
- [Acceptance recipe](#acceptance-recipe)
- [Evaluation record](#evaluation-record)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Hosted MCP; see official connector setup | Yes | [check](https://www.wireflow.ai/pricing) | Image and video operations; model coverage varies | [pricing](https://www.wireflow.ai/pricing) | n/a |
| **[Flora AI](#2-flora-ai)** | Hosted MCP with OAuth | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[Krea AI](#3-krea-ai)** | n/a | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[Freepik Spaces](#4-freepik-spaces)** | Magnific hosted MCP; follow current official setup | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[n8n](#5-n8n)** | n/a | Yes | n/a | Orchestration of connected models and services | n/a | [n8n-io/n8n](https://github.com/n8n-io/n8n), 207,099 ★, n8n@2.42.7 |
| **[Flowise](#6-flowise)** | n/a | Yes | n/a | Orchestration of connected models and services | n/a | [FlowiseAI/Flowise](https://github.com/FlowiseAI/Flowise), 55,494 ★, flowise@3.1.4 |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | Visual graph | REST API | Workflow execution API | Self-hosted runtime | Score |
|------|---|---|---|---|-------|
| **[Flowise](#6-flowise)** | ✅ | ✅ | ✅ | ✅ | **4/4** |
| **[Wireflow](#1-wireflow)** | ✅ | ✅ | ✅ | n/a | **3/4** |
| **[Flora AI](#2-flora-ai)** | ✅ | ✅ | ✅ | n/a | **3/4** |
| **[Krea AI](#3-krea-ai)** | ✅ | ✅ | ✅ | n/a | **3/4** |
| **[n8n](#5-n8n)** | ✅ | ✅ | n/a | ✅ | **3/4** |
| **[Freepik Spaces](#4-freepik-spaces)** | ✅ | ✅ | n/a | n/a | **2/4** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. Wireflow

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** A hosted canvas for connected image, video and audio operations, with workflow execution APIs.
- **Limits:** Check credits, model inputs and execution limits for the actual workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.wireflow.ai)
  - [Wireflow AI workflow builder page](https://www.wireflow.ai/ai-workflow-builder)
  - [Docs](https://www.wireflow.ai/docs)
  - [Pricing](https://www.wireflow.ai/pricing)
  - [Official source 1](https://www.wireflow.ai/docs/creating-workflows)
  - [Official source 2](https://www.wireflow.ai/docs/api/run)
  - [Official source 3](https://www.wireflow.ai/docs/mcp)
  - [Official source 4](https://www.wireflow.ai/docs/batch-image-generation)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.wireflow.ai/docs
```

### 2. Flora AI

![Flora AI screenshot](https://assets.wireflow.ai/competitors/flora-2cd907d1b38c.png?v=r5)

- **What it is:** A creative canvas with reusable Techniques, API access and a hosted MCP interface.
- **Limits:** A saved Technique must expose suitable inputs; check billing and account access before running it.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://flora.ai)
  - [Docs](https://developer.flora.ai/api/)
  - [Official source 2](https://developer.flora.ai/mcp/)
  - [Official source 3](https://developer.flora.ai/quickstarts/cli/)

Official CLI installation; this installs software but submits no generation:
```bash
go install github.com/florafauna-ai/flora-cli/cmd/flora@latest
```

### 3. Krea AI

![Krea AI screenshot](https://assets.wireflow.ai/competitors/krea-ai-bfc62405e654.png?v=r5)

- **What it is:** Creative model APIs alongside a Nodes canvas for image, video and audio workflows.
- **Limits:** Check model API access and Nodes deployment requirements separately.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.krea.ai)
  - [Docs](https://www.krea.ai/docs/developers/introduction)
  - [Official source 2](https://www.krea.ai/docs/user-guide/features/nodes)
  - [Official source 3](https://www.krea.ai/docs/api-reference/node-apps/execute-a-node-app)
  - [Official source 4](https://www.krea.ai/docs/api-reference/image-enhance/krea-enhance)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.krea.ai/docs/developers/introduction
```

### 4. Freepik Spaces

![Freepik Spaces screenshot](https://assets.wireflow.ai/competitors/freepik-spaces-01abfb6e9731.png?v=r5)

- **What it is:** Now part of Magnific: a shared image/video canvas alongside documented media APIs and MCP access.
- **Limits:** Confirm the current interface and account access for the exact saved workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. The older indexed Apps API guide returned 404 after redirecting to Magnific on 2026-09-21. Current full-workflow REST execution was not established in this review; this is uncertainty, not a claim that the capability is absent.
- **Links:**
  - [Homepage](https://www.magnific.com/spaces)
  - [Docs](https://docs.magnific.com/introduction)
  - [Official source 3](https://www.magnific.com/blog/magnific-mcp-chatgpt/)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.magnific.com/introduction
```

### 5. n8n

![n8n screenshot](https://assets.wireflow.ai/competitors/n8n-9d3655cbb45e.png?v=r5)

- **What it is:** A visual automation system for connecting services, data and AI calls.
- **Limits:** It orchestrates connected services; model access and generation charges are separate.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. Self-hosting is available under n8n licensing terms; do not describe every commercial use as unrestricted open source.
- **Links:**
  - [Homepage](https://n8n.io)
  - [Docs](https://docs.n8n.io)
  - [n8n-io/n8n](https://github.com/n8n-io/n8n)
  - [Official source 2](https://docs.n8n.io/hosting)
  - [Official source 3](https://docs.n8n.io/api)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.n8n.io
```

### 6. Flowise

![Flowise screenshot](https://assets.wireflow.ai/competitors/flowise-0a3b77ed943a.png?v=r5)

- **What it is:** A visual builder for AI agents and flows with a prediction API.
- **Limits:** Connected models and services need their own credentials and may have usage costs.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://flowiseai.com)
  - [Docs](https://docs.flowiseai.com)
  - [FlowiseAI/Flowise](https://github.com/FlowiseAI/Flowise)
  - [Official source 2](https://docs.flowiseai.com/api-reference/prediction)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.flowiseai.com
```

## Decision this list supports

An agency needs repeatable client delivery with clear inputs and ownership. Compare the creative process separately from the automation that moves briefs and files between systems.

## Scope and evidence

Documentation reviewed on 2026-09-21. This is a Wireflow-maintained resource dataset. Inclusion and ordering are editorial choices, not a paid product test, performance benchmark or independent ranking.

The capability score counts positively documented checks. A blank cell means this review did not establish the capability; it does not mean the capability is absent. Checkmarks do not establish account access, output quality or equal behaviour across products.

The weekly repository job refreshes GitHub metadata. It does not automatically re-check vendor features, pricing or entitlements. Follow the official links for current terms.

## Selection notes

Hosted creative canvases suit asset production. n8n suits connections between operational systems; Flowise suits agent and AI-flow logic. Neither orchestration category automatically supplies a polished creative deliverable.

## Acceptance recipe

1. Write a client input form with required assets, output formats and approval owner.
2. Build one complete deliverable before introducing several campaign branches.
3. Test a missing asset and a rejected creative result as different failure cases.
4. Have a second teammate rerun the process from the written inputs.
5. Check credential ownership and access removal when a client or teammate leaves.
6. Include review time and correction work in the delivery cost.

## Evaluation record

Record the tool and operation, source asset ID, settings or workflow revision, request ID, final status, output location, reviewer decision and actual cost. Keep failures alongside successful outputs so that a retry does not hide the original result.

## How this list is maintained

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run, so edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE), public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
