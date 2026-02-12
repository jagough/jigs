---
layout: default
title: Home
nav_order: 1
permalink: /
---

# JIGs

> *A jig is a type of custom-made tool used to control the location or motion of parts or other tools. A jig's primary purpose is to provide repeatability, accuracy, and interchangeability in the manufacturing of products.*

**Jonathan's Implementation Guidance** — structured, opinionated documentation for HTTP API service design and development.

## What are JIGs?

JIGs are concise, numbered documents that capture implementation decisions, patterns, and standards. Inspired by [Google's API Improvement Proposals (AIPs)](https://google.aip.dev/), JIGs are tailored for **HTTP API services** rather than gRPC.

Each JIG follows a consistent format with guidance, examples, anti-patterns, and rationale, using [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119) keywords to clearly convey requirements.

## Dual-audience design

JIGs are written to be useful for both:

- **Human developers** — as readable reference documentation for design decisions
- **AI agents** — as structured, machine-parsable guidance that can be applied autonomously (e.g. via MCP servers)

## JIG categories

| Number range | Category              | Description                              |
|--------------|-----------------------|------------------------------------------|
| 1–99         | General / Meta        | JIG purpose, numbering, style guidance   |
| 100–999      | API Design            | Resource naming, errors, CRUD patterns   |
| 1000–1999    | Service Architecture  | *(reserved for future use)*              |

## Writing a new JIG

1. Copy `jigs/template.md`
2. Assign the next available number in the appropriate range (see [JIG-2: Numbering]({% link jigs/general/0002.md %}))
3. Follow the style rules in [JIG-8: Style and Guidance]({% link jigs/general/0008.md %})
4. Place the file in the matching category directory
