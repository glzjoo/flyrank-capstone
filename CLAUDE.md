# CLAUDE.md

Guidance for AI assistants (Claude Code, Cursor) working in this repo.

## Project
Capstone for the FlyRank Frontend AI Engineering internship. A single-page React app; features are added week by week.

## Stack
- React 19 + TypeScript (strict), built with Vite 8
- Linting: oxlint (`.oxlintrc.json`)
- Package manager: npm (commit `package-lock.json`)
- Node: current LTS or newer

## Commands
- `npm install`: install dependencies
- `npm run dev`: start the dev server (http://localhost:5173)
- `npm run lint`: run oxlint
- `npm run build`: type-check (`tsc -b`) then build to `dist/`
- `npm run preview`: serve the production build

Run `npm run lint` and `npm run build` before every commit. Both must pass.

## Structure
- `src/main.tsx`: app entry point
- `src/App.tsx`: root component
- `src/assets/`: images and SVGs imported by components
- `public/`: static files served as-is
- New components go in `src/components/`, one component per file, named in PascalCase (`UserCard.tsx`)

## Code conventions
- Function components and hooks only; no class components
- Type props explicitly; avoid `any`, prefer `unknown` plus narrowing
- Named exports for components, except pages and entry files
- Keep components small; extract a hook when logic is reused
- No new dependencies without a reason stated in the commit message
- Never hard-code secrets; read config from `import.meta.env.VITE_*` and keep `.env` out of git

## Git conventions
Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/): `type(scope): imperative summary`.
- Types: `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `style`, `build`, `ci`
- Subject under 72 characters, lower case, no trailing period
- One logical change per commit; do not squash or rewrite published history
- Example: `feat(auth): add login form validation`

## Do not touch
- `package-lock.json`: change it only through npm commands
- `.env*` files and anything in `dist/` or `node_modules/`
- `LICENSE`

## When making changes
- Make the smallest change that solves the task and match the surrounding style
- Explain what you changed and why; flag anything you could not verify
