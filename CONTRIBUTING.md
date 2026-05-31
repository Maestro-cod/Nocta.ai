# Contributing to Lumen

Thanks for your interest in making Lumen better. 💜

## Development workflow

1. Fork the repo and clone your fork.
2. Create a feature branch: `git checkout -b feat/short-description`.
3. Install deps: `npm install`.
4. Run the dev server: `npm run dev`.
5. Make your changes. Keep components small and TypeScript strict.
6. Run the production build: `npm run build`. This is the CI gate.
7. Commit using [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat(feed): add double-tap to like`
   - `fix(profile): handle empty bio`
   - `docs: update Play Store checklist`
8. Open a pull request against `main`.

## Style guide

- TypeScript strict mode is on. `any` is allowed only when explicitly commented.
- Prefer Tailwind utility classes. Add tokens to `src/index.css` under `@theme`.
- Keep components below 300 lines; split into smaller files when needed.
- No runtime dependencies should be added to `package.json` without a PR rationale.
- Use emojis as icons — zero-runtime icon set keeps the bundle tiny.

## Pull request checklist

- [ ] `npm run build` passes.
- [ ] New components / pages are reachable from the bottom nav or a sub-route.
- [ ] Keyboard & screen-reader basics (labels, roles, focus).
- [ ] Works on iPhone SE (375×667) and desktop (1440×900).
- [ ] Any new config / env var is mirrored in `.env.example`.

## Reporting bugs

Open an issue with:
- Device + OS + browser / app version
- Steps to reproduce
- Expected vs. actual
- Screenshot / short video if possible

## Security disclosures

See [`SECURITY.md`](./SECURITY.md).
