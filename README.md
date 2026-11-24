# flyrank-capstone

Capstone project for the FlyRank **Frontend AI Engineering** internship track: a React + TypeScript web app, built week by week with an AI-assisted workflow (Claude Code).

> Status: Week 1 (environment and toolchain setup). Project scope will be filled in as the track progresses.

## Tech stack

| Area | Tool |
| --- | --- |
| UI | React 19 |
| Language | TypeScript |
| Build tool | Vite |
| Linting | oxlint |
| AI assistant | Claude Code |

## Getting started

**Prerequisites:** Node.js (LTS or newer) and Git.

```bash
git clone https://github.com/glzjoo/flyrank-capstone.git
cd flyrank-capstone
npm install
npm run dev
```

Then open http://localhost:5173.

## Project structure

```text
src/
  main.tsx        App entry point
  App.tsx         Root component
  assets/         Images and SVGs imported by components
  components/     One component per file, PascalCase (added as features land)
public/           Static files served as-is
```

## Scripts

| Command | What it does |
| --- | --- |
| `npm run dev` | Start the dev server with hot reload |
| `npm run lint` | Lint the code with oxlint |
| `npm run build` | Type-check and create a production build in `dist/` |
| `npm run preview` | Preview the production build locally |

## Contributing and workflow

- Commits follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), for example `feat(ui): add header component`.
- Project conventions for humans and AI assistants live in [CLAUDE.md](CLAUDE.md).
- Run `npm run lint` and `npm run build` before committing.

## License

[MIT](LICENSE)
