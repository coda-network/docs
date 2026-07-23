# Repository Guidelines

## Project scope and structure

This repository contains the public, English-language documentation for Coda, built with Mintlify. Documentation pages are MDX files in the repository root or in topic-specific directories. Each page begins with YAML frontmatter that defines its title, description, and optional navigation metadata.

`docs.json` is the source of truth for site configuration, navigation, branding, and integrations. Update it whenever you add, remove, rename, or move a navigable page. Put static assets in the location referenced by `docs.json` or the relevant MDX page.

`style-test.mdx` is an approved public visual-test and component-reference page. Keep it available for maintenance and visual review, but do not include it in primary navigation. Do not publish other internal test, component-demo, or visual-style pages.

## Repository language policy

Use English exclusively for all persisted repository content. This includes documentation, frontmatter, configuration, code samples, comments, issue discussions, commit messages, and pull request text. Translate non-English input into English before saving it.

## Governance files

`AGENTS.md` is the canonical source of governance for this repository. `CLAUDE.md` must remain a thin Claude Code adapter that imports `AGENTS.md`; do not duplicate shared instructions there.

Do not add other repository governance files unless a maintainer explicitly changes this policy. Keep tool-specific permissions, hooks, and settings in the relevant tool configuration rather than in these files.

## Public contribution policy

This is a public repository, but external contributions are accepted through GitHub issues only. Do not accept or create external pull requests for content changes. Ask external contributors to open an issue that states the affected page, the problem, the proposed correction, and supporting public evidence where relevant.

Maintainers may make documentation changes directly after assessing an issue. Keep each change narrowly scoped to a coherent documentation outcome.

## Documentation standards

Write for developers and institutional operators who use Coda.

- Use active voice and address the reader as “you.” Keep sentences concise and express one idea per sentence.
- Use sentence case for headings. Use descriptive page titles and task-oriented descriptions.
- Use **bold** for UI labels and `code` formatting for file names, paths, commands, API fields, environment variables, values, and code references.
- Prefer a short introduction, prerequisites, ordered steps, expected outcomes, and relevant next steps when documenting a workflow.
- Use Mintlify components only when they improve scanning or comprehension. Use `Note` for context, `Warning` for consequential prerequisites or limitations, and `Danger` only for material risk.
- Ensure every link, heading anchor, code fence language, and referenced page path is valid. Prefer relative links for pages in this site.
- Write accurate, implementation-ready examples. Explain placeholders, expected responses, and errors where relevant.

## Content authority and boundaries

Documentation authors decide the content of general public documentation. Use sound editorial judgment, prefer verified public information, and correct inaccuracies promptly.

Use the following product language consistently:

- Use “Coda” for both the company and product name.
- Render the logo and wordmark as “CODA”; use “Coda” in prose.
- Use “institution” for the organization defining policy.
- Use “decision” for an `ALLOW`, `REVIEW`, or `DENY` outcome. Write those outcomes in uppercase.
- Use “digital asset interaction” when describing wallet creation, signing, deposits, or withdrawals together.
- Do not describe Coda as custody, analytics, a system of record, or a source of blockchain intelligence.

Publish only current, public concepts and workflows. Do not publish credentials, access tokens, private endpoints, customer data, internal operating procedures, unapproved roadmap details, or security details that would aid abuse. Use clearly marked placeholders, such as `CODA_API_KEY`, and never include realistic secrets.

## API and integration documentation

Publish integration documentation only when the relevant APIs, fields, workflows, and examples have been approved for public use. Use stable, approved sources for endpoint details and schemas. Do not infer, invent, or expose undocumented capabilities.

Examples must be safe to copy, use non-production credentials and data, and clearly identify placeholders. Describe the supported behavior only; do not add availability, certification, security, or compliance commitments unless they are approved for public publication.

## Versioning and lifecycle

The site documents the current public product only. Do not create parallel documentation trees for historical product or API versions. Update the affected page when public behavior changes, remove obsolete instructions, and rely on Git history to preserve prior content.

## Validation and local development

Use Mintlify's MCP server to edit documentation and configuration when it is available. Use the Mintlify documentation MCP server or official Mintlify documentation to confirm component and configuration behavior when needed.

Use the Mintlify CLI to preview documentation locally:

- `mint dev` starts a local preview from the directory containing `docs.json`.
- `mint update` updates the CLI when troubleshooting a local preview issue.

Validate changes according to their risk:

- For copy-only changes, verify frontmatter, terminology, links, code formatting, and factual accuracy.
- For navigation, component, layout, or code-block changes, inspect the changed page in a local Mintlify preview.
- For integration documentation, also verify that the content remains within the approved public API and product scope.

If the required CLI is unavailable, state the validation limitation in the relevant issue or maintainer handoff.
