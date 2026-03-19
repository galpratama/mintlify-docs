# AGENTS.md

Repository guidance for agents working in `/Users/galpratama/Development/galpratama/belajarkoding-docs`.

## Project summary

This repository is the public documentation portal for BelajarKoding, built with [Mintlify](https://mintlify.com).

Current documentation scope:

- Product portal home page at `index.mdx`
- English portal home page at `en/index.mdx`
- Dedicated product documentation for KilatKoding under `kilatkoding/`
- English KilatKoding documentation under `en/kilatkoding/`
- Site-wide configuration in `docs.json`

The navigation is organized by product. KilatKoding must remain visible as its own dedicated product section in `docs.json`.

## Primary source of truth

When documenting KilatKoding, use the application repository as the source of truth:

- `/Users/galpratama/Development/galpratama/kilatkoding-src`

Check these files first before writing or updating docs:

- `README.md`
- `.env.example`
- `package.json`
- `config/*`
- `app/*`
- `lib/*`
- `supabase/migrations/*`
- `docs/en/*`
- `docs/id/*`

Do not invent features, routes, or configuration that are not present in the codebase.

## Mintlify workflow

- Pages are MDX files with YAML frontmatter.
- Every new page must be added to `docs.json`, or it will not appear in navigation.
- Prefer Mintlify built-in components such as `Card`, `Columns`, `Steps`, `Accordion`, `Info`, `Tip`, `Warning`, and `Note`.
- If you change navigation, layout, or `docs.json` behavior, verify against official Mintlify docs first.
- Use root-relative internal links without file extensions, for example `/kilatkoding/local-setup`.

Useful commands:

```bash
mint dev
npx mint validate
npx mint broken-links
```

If Mintlify CLI validation fails because of outdated local framework assets, run:

```bash
npx mint update
```

## Information architecture rules

- Keep `index.mdx` as the BelajarKoding docs portal page.
- Keep `en/index.mdx` as the English portal page.
- Keep KilatKoding docs inside the `kilatkoding/` directory.
- Keep English KilatKoding docs inside the `en/kilatkoding/` directory.
- If another product is added later, give it its own dedicated product entry in `docs.json`.
- Do not mix multiple products into the same product navigation group.
- Prefer shallow, readable groupings over deeply nested navigation.

## Audience and writing style

This documentation is written for both non-technical and technical readers.

Write with these rules:

- Maintain Indonesian and English versions in parallel for KilatKoding docs
- Primary language for the default site tree: Bahasa Indonesia
- Use active voice and second person
- For Indonesian docs, use "kamu" instead of "Anda" and keep the tone clear, friendly, and slightly informal
- Keep sentences concise
- Explain what something is before explaining how to use it
- Prefer plain language before technical jargon
- When setup is involved, include steps for Windows, macOS, and Linux where relevant
- Clearly separate required items from optional items
- Use exact names for routes, commands, env vars, files, and config values
- Use bold for UI labels and backticks for commands, paths, env vars, and code references

## Terminology

Use these terms consistently:

- "produk" for a documented offering in this portal
- "boilerplate" for KilatKoding itself
- "setup lokal" for local development setup
- "environment variables" for env configuration
- "user" for end users of the product
- "admin" for internal operators with elevated access
- "payment provider" for Midtrans or Doku

Avoid swapping between multiple terms for the same concept without a reason.

## Content boundaries

- Document the current behavior of the codebase, not an ideal future state.
- Mark roadmap or planned functionality clearly as not yet available.
- Do not expose secrets, private keys, or sensitive internal values.
- Do not claim that a feature is production-ready unless the repository already supports it.
- Do not remove existing reference pages unless the change is intentional and navigation is updated accordingly.

## Update expectations

When documentation changes materially:

1. Update or add the relevant MDX page.
2. If the page is part of KilatKoding docs, update both `kilatkoding/` and `en/kilatkoding/` unless the user explicitly asks for a single language only.
3. Update `docs.json` navigation if needed.
4. Check internal links.
5. Run `npx mint validate`.
6. Run `npx mint broken-links`.

## Current product coverage

KilatKoding docs currently cover:

- product overview
- onboarding and setup planning
- local setup across operating systems
- service setup and env vars
- features, routes, and customization
- UI, architecture, database, deployment, and troubleshooting

This coverage now exists in both Indonesian and English.

Preserve this structure unless there is a clear documentation reason to reorganize it.
