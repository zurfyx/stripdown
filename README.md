# Stripdown

Convert Markdown to **unstyled** rich text and copy it to your clipboard. The output preserves structure (headings, lists, tables, code, links) but carries no opinionated fonts, colors, or sizes — paste it anywhere and it inherits the destination's styling.

Live: https://stripdown.vercel.app/

## Stack

- React 19 + TypeScript + Vite
- Tailwind CSS v4 + shadcn/ui (Radix primitives)
- `marked` for Markdown parsing
- Vitest for tests

## Develop

```bash
pnpm install
pnpm dev          # http://localhost:3000
pnpm test         # run unit tests
pnpm typecheck    # tsc --noEmit
pnpm lint         # prettier --check
pnpm build        # static site → dist/
```

## Deploy

Hosted on Vercel. Pushes to `main` deploy to production; pull requests get preview deployments. Build settings live in `vercel.json`. CI on every push and PR runs lint, typecheck, test, and build via `.github/workflows/ci.yml`.

## License

MIT
