# Agentic AI Security Control Framework checklist

An interactive checklist for securing agentic AI systems: systems where a model plans or acts through tools, memory, protocols or other agents. It turns the treatment measures in the Cyber Security Agency of Singapore's *Securing Agentic AI: An Addendum to the Guidelines and Companion Guide on Securing AI Systems* (Chapter 4.3) into a tiered, assessable checklist, and incorporates the *Companion Guide on Securing AI Systems*.

**Open the checklist:** https://joshuacsa.github.io/Agentic-AI-Security-Control-Framework-checklist/

Version 0.7 (draft), 28 October 2026. 139 measures in 24 controls, across five lifecycle stages: planning and design, development, deployment, operations and maintenance, and end of life.

---

## How to use it

### Step 1: Describe the system

Name the system in the header, then answer the questions in *Step 1: Describe the system*. Each question covers an element of the Addendum's capability taxonomy, such as code execution, memory or agent delegation.

- **No** removes the measures that question triggers.
- **Yes** or **Not sure** keeps them, so the list only shrinks when someone actively rules something out.

### Step 2: Set the sourcing

Under **Sourcing**, choose how the system is sourced: SaaS agent, agent platform, own agent on a model API, or self-hosted. This sets who provides each layer of the system, and each measure's default owner follows its layer. Change any layer this vendor handles differently.

### Step 3: Choose the risk class

Use the **Risk class** toggle in the bar at the top. The **lethal trifecta** check below Step 1 flags systems that combine access to private data, exposure to untrusted content and a way to send data out, and suggests High.

### Step 4: Work through the measures

Tick each measure's checks, or the box beside it when it has none. Mark anything that does not apply as not applicable, and add notes as evidence. Each measure lists the evidence an assessor should see, and many link to references and tools.

### Step 5: Confirm who does each measure

Change a measure's owner where it differs from its layer's default.

- **To confirm:** use until the vendor answers.
- **Gap:** use where nobody covers the measure. A gap needs a compensating control or formal risk acceptance.

The left panel counts measures by owner; click a count to show only those measures.

### Step 6: Ask vendors for evidence

**Vendor questionnaire** downloads every measure the vendor does, shares or has yet to confirm, phrased as requests and ready to send. Mark measures met once you accept the vendor's evidence.

### Step 7: Save and share

Progress is kept in your browser.

- **Save to file** keeps or shares an assessment, and **Open file** loads one.
- **Download CSV** exports the filtered list.

---

## Levels and risk classes

### Levels

| Level | Meaning |
|---|---|
| **L0 Fundamental** | Minimum hygiene without which an agent should not run in production |
| **L1 Standard** | Needs design effort and must be adapted meaningfully to the system |
| **L2 Best practice** | Advanced or emerging measures for defence in depth |

### What each risk class requires

| Risk class | L0 | L1 | L2 |
|---|---|---|---|
| **High** | Mandatory | Mandatory (tailored) | Each measure assessed: adopt, or record why not |
| **Moderate** | Mandatory | Mandatory (tailored) | Considered where the risk assessment shows a gap |
| **Low** | Mandatory | Recommended where relevant | Optional |

The checklist lists the triggers for each class under *How to use this checklist*. The highest class whose trigger applies wins, and an unclassified system is treated as High.

---

## What each measure shows

| Element | What it tells you |
|---|---|
| **For systems with / Applies when** | The profile questions, or sourcing conditions, that make the measure apply. Measures with no tags apply to every system. |
| **Layer and owner** | The part of the system the measure acts on, such as the agent runtime or the model, and who does it for this system. |
| **Requirement** | What the chosen risk class requires of the measure's level. |
| **Threats addressed** | Shown on each control: the threats it addresses, from a combined taxonomy of the OWASP LLM, Agentic Applications, MCP and Agentic Skills Top 10s. Hover over a threat for its description. |
| **References** | Guidance and tools from the source documents, with links. Named tools are examples to start from, not endorsements. |

---

## Sources

- Cyber Security Agency of Singapore, *Securing Agentic AI: An Addendum to the Guidelines and Companion Guide on Securing AI Systems*, v1.0, June 2026
- Cyber Security Agency of Singapore, *Companion Guide on Securing AI Systems* (50 of its 51 measures are covered)
- Microsoft, *AI agent shared responsibility model*, for the layers and sourcing presets, cross-checked with the Coalition for Secure AI's *AI Shared Responsibility Framework*
- OWASP Top 10 for LLM Applications, Top 10 for Agentic Applications 2026, MCP Top 10 and Agentic Skills Top 10, for the threats and the lethal trifecta

---

## Running it locally

The checklist is a single self-contained HTML file. Download `index.html` and open it in a browser; it needs no server or installation. It loads the IBM Plex Sans font from Google Fonts and falls back to system fonts when offline.
