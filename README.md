# Coda Network documentation

This repository contains the public product documentation published at
`https://doc.codanetwork.io/`.

## Content policy

- Keep public claims aligned with approved Coda Network product copy.
- Keep `style-test.mdx` available as the explicitly approved public visual-test
  page. Do not remove it without explicit maintainer approval.
- Do not publish other test, component-demo, or visual-style pages.
- Do not publish API contracts, security claims, or availability commitments
  without the required product and security approval.
- Request review for every change before merging it into `main`.

## Local preview

Install the [Mintlify CLI](https://www.npmjs.com/package/mint), then run it from
the repository root:

```bash
mint dev
```

View the local preview at `http://localhost:3000`.

## Publishing

Mintlify publishes changes from the default branch. Merge only approved content,
then verify the production index and all navigation destinations.
