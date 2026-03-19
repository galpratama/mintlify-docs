# BelajarKoding Docs

This repository contains the public documentation portal for BelajarKoding, built with Mintlify.

Current scope:

- portal landing page for BelajarKoding docs
- dedicated product documentation for KilatKoding in Indonesian and English

## Local development

Install the Mintlify CLI if needed:

```bash
npm i -g mint
```

Run the docs locally from the repository root:

```bash
mint dev
```

The local preview is available at `http://localhost:3000`.

## Validation

Before publishing documentation changes, run:

```bash
npx mint validate
npx mint broken-links
```

If the Mintlify CLI has local framework asset issues, run:

```bash
npx mint update
```

## Documentation structure

- `index.mdx` is the BelajarKoding docs portal page
- `en/index.mdx` is the English portal page
- `kilatkoding/` contains the Indonesian KilatKoding docs
- `en/kilatkoding/` contains the English KilatKoding docs
- `docs.json` controls site navigation and global Mintlify settings

## Source of truth for KilatKoding docs

KilatKoding documentation in this repo should be based on:

- `/Users/galpratama/Development/galpratama/kilatkoding-src`

## Mintlify skill

If you want up-to-date Mintlify guidance for components and configuration:

```bash
npx skills add https://mintlify.com/docs -g -y
```
