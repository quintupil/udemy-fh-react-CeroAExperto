# Project Structure

```
04-hooks-app/
├── src/
│   ├── 01-useState/        # useState lesson components
│   ├── 02-useEffect/       # useEffect lesson components
│   ├── 03-examples/        # composed hook examples (e.g. PokemonPage)
│   ├── 04-useRef/          # useRef lesson components
│   ├── hooks/              # shared custom hooks
│   ├── HooksApp.tsx        # root app component
│   ├── main.tsx            # entry point — swap active component here
│   └── index.css           # global styles + Tailwind import
```

## Conventions

- Components use named exports (`export const MyComponent = () => ...`), never default exports
- Custom hooks live in `src/hooks/` and are named `use<Name>.ts` (plain `.ts`, not `.tsx`)
- Components are `.tsx` files; hooks and utilities are `.ts`
- Lesson folders are numbered (`01-`, `02-`, etc.) to reflect course progression
- New lessons get their own numbered subfolder under `src/`
- `main.tsx` uses comment-toggling to switch the active lesson component — keep unused imports commented, not deleted
- Tailwind utility classes are used directly in JSX; no CSS modules or styled-components
- Custom Tailwind component classes (e.g. `.bg-gradient`) are defined in `index.css` using `@apply`
- Hooks return an object with props and methods grouped and commented (see `useTrafficLight.ts` as reference)
- Types derived from object keys use `keyof typeof obj` pattern instead of manual union types
