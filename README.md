## Next.js App Router Template

A ready-to-use template for building Next.js (App Router) apps with Tailwind CSS, Prettier, ESLint, Husky, and lint-staged preconfigured. It includes format-on-save and lint-on-save settings for VS Code/Cursor and a pre-commit workflow to keep your codebase clean.

### Features

- **Next.js (App Router)** with TypeScript
- **Tailwind CSS** (v4)
- **ESLint** (Next.js config + TypeScript) with **eslint-config-prettier**
- **Prettier** for opinionated formatting
- **Husky + lint-staged** pre-commit hooks
- **Format on save** and **ESLint fix on save** via `.vscode/settings.json`
- **Node version**: engines set to `>=22.19.0` with `.nvmrc`

### Requirements

- Node.js `>=22.19.0` (recommended: `nvm use` in project directory)

### Getting Started

Install dependencies and start the dev server:

```bash
npm install
npm run dev
```

Open `http://localhost:3000` and start editing `src/app/page.tsx`.

### Scripts

- `npm run dev` — start Next.js in development
- `npm run build` — build for production
- `npm run start` — start production server
- `npm run lint` — run ESLint
- `npm run lint:fix` — run ESLint with auto-fix
- `npm run format` — format all files with Prettier
- `npm run format:check` — check formatting without writing

### Pre-commit Hooks

Husky and lint-staged run on each commit:

- JavaScript/TypeScript files: `eslint --fix` and `prettier --write`
- JSON/CSS/SCSS/Markdown: `prettier --write`

Commits are blocked on ESLint errors; warnings do not fail commits by default.

### Editor Integration (VS Code/Cursor)

This repo includes `.vscode/settings.json` with:

- `editor.formatOnSave: true`
- Prettier as default formatter
- ESLint fix on save (`source.fixAll.eslint`)

Install the Prettier extension (`esbenp.prettier-vscode`) for best results.

### Project Structure

```
src/
  app/           # Next.js App Router (layouts, pages, etc.)
public/          # Static assets
```

### Notes

- Node version is enforced via `"engines"` in `package.json` and `.nvmrc`.
- Tailwind v4 is configured via `@tailwindcss/postcss` and `src/app/globals.css`.

You're ready to build. Happy shipping!
