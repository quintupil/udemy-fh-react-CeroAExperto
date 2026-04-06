# Tech Stack

## Core
- React 19 with TypeScript (strict mode)
- Vite 7 + SWC compiler (`@vitejs/plugin-react-swc`)
- Tailwind CSS v4 (via `@tailwindcss/vite` plugin)

## Tooling
- ESLint 9 with `typescript-eslint`, `eslint-plugin-react-hooks`, `eslint-plugin-react-refresh`
- TypeScript 5.9 with strict settings (`noUnusedLocals`, `noUnusedParameters`, `strict: true`)

## Path Aliases
`@/` maps to `./src/` — use it for imports instead of relative paths when outside the same folder.

## Common Commands

Run from `04-hooks-app/`:

```bash
npm run dev       # start dev server
npm run build     # type-check + production build
npm run lint      # run ESLint
npm run preview   # preview production build
```
