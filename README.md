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

## Repository structure

```
jigs/
├── template.md          # Standard template for new JIGs
├── general/             # Meta-JIGs and cross-cutting guidance
│   ├── 0001.md          # JIG Purpose and Guidelines
│   ├── 0002.md          # JIG Numbering
│   └── 0008.md          # JIG Style and Guidance
└── api-design/          # API design patterns
    ├── 0122.md          # Resource Names
    ├── 0123.md          # Resource Types
    ├── 0124.md          # Listing Resources
    ├── 0126.md          # Custom Methods
    ├── 0129.md          # Error Handling Basics
    ├── 0130.md          # HTTP Errors
    ├── 0131.md          # Common Custom Methods
    ├── 0132.md          # Partial Update
    ├── 0133.md          # Deletion
    ├── 0134.md          # Undelete Operations
    └── 0135.md          # Batch Operations
```

## Writing a new JIG

1. Copy `jigs/template.md`
2. Assign the next available number in the appropriate range (see [JIG-0002](jigs/general/0002.md))
3. Follow the style rules in [JIG-0008](jigs/general/0008.md)
4. Place the file in the matching category directory
