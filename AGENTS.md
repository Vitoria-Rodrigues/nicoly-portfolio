# Nicoly Portfolio Agents Context

This document serves as the sovereign root context router (Layer 1) for AI agents operating in the `Vitoria-Rodrigues/nicoly-portfolio` repository.

## Navigation

- [README.md](./README.md): Primary developer documentation, architecture overview, and Vercel CI/CD workflow guide.
- [.agents/plugins.json](./.agents/plugins.json): Antigravity plugin registry importing domain plugins from `@vitoria-rodrigues/agent-mesh`.
- [pnpm-workspace.yaml](./pnpm-workspace.yaml): Centralized dependency catalogs (`catalogMode: strict`) and `@vitoria-rodrigues/agent-mesh` registration.
- [package.json](./package.json): Scoped package manifest (`@vitoria-rodrigues/nicoly-portfolio`) and TypeScript/Vite scripts.
- [.github/workflows/vercel-deploy.yml](./.github/workflows/vercel-deploy.yml): Continuous integration (`pnpm lint`, `pnpm build`) and Vercel production deployment pipeline.

## Architecture

The application is an interactive portfolio web application built with React 19.3, TypeScript 6.0, React Three Fiber, React Router 8, and Vite 8.3:

- **`src/App.tsx`**: Root application shell mounting navigation and portfolio views.
- **`src/components/layout/`**: Structural layout components (`NavBar/`).
- **`src/components/ui/`**: Reusable UI primitives (`Button/`, `Card/`, `MapModal/`, `ThemeToggle/`) scoped with CSS Modules (`*.module.css`).
- **`src/assets/`**: Visual and map media assets.
- **TypeScript & Build**: Solution-style `tsconfig.json` referencing `tsconfig.app.json` and `tsconfig.node.json` compiled via `tsc -b && vite build`.

## Scoped Guardrails

- MUST maintain a strict senior, objective, and technical tone across all communications, documentation, and code.
- MUST conduct conversational chat responses in Brazilian Portuguese (pt-BR) while keeping all code, configuration files, commit messages, and technical documentation in English (en-US).
- MUST NOT use emojis anywhere in code, markdown headers, body text, commit messages, or chat responses (Zero-Emoji Invariant).
- MUST use `pnpm` exclusively and consume all dependencies via `catalog:` entries in `pnpm-workspace.yaml` (never raw semver strings in `package.json`).
- MUST consume `@vitoria-rodrigues/agent-mesh` solely via `catalog:plugins-stack` and `.agents/plugins.json` without duplicating local skills or rules inside `.agents/`.
- MUST ensure `pnpm lint` and `pnpm build` (`tsc -b && vite build`) pass before pushing changes to `main` or opening Pull Requests.
- MUST use Conventional Commits v1.0.0 (`<type>(<scope>): <description>`) and sign commits with SSH (`git commit -S -m "..."`) when `user.signingkey` is configured.
- MUST use relative paths for all Markdown links inside repository files.

## Required Skills

When operating in this repository, agents MUST activate the relevant `@vitoria-rodrigues/agent-mesh` skill:

- **`router-architect`**: Active when authoring or auditing `AGENTS.md` context routers.
- **`readme-architect`**: Active when updating or auditing `README.md` documentation.
- **`monorepo-architect`**: Active when auditing `pnpm-workspace.yaml` catalogs or `package.json` manifests.
- **`github-flow-operator`**: Active when creating branches, commits, or pull requests, or troubleshooting CI workflows.
- **`browser-auditor`**: Active when inspecting 3D Three.js scenes, responsive layouts, or modal interactions in a browser.
