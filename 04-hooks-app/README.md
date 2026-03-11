# 04-hooks-app

## Instalar y configurar Tailwindcss

**https://tailwindcss.com/**

1. Install Tailwindcss

```bash
npm install tailwindcss @tailwindcss/vite
```

2. Agregar en archivo **vite.config.ts**
   Add the @tailwindcss/vite plugin to your Vite configuration.

```
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite' //Agregar esta linea

export default defineConfig({
  plugins: [
    tailwindcss(), //Agregar esta linea
  ],
})
```

3. Import Tailwind CSS
   Add an @import to your CSS file (**index.css**) that imports Tailwind CSS.

```
@import "tailwindcss";
```

4. Agregar estilos :

Recurso:
**https://gist.github.com/Klerith/8a5440ab34058b22e4874e01e7e931a0**

Copiar contenido y pegar en **index.css**

```bash
@import "tailwindcss";

.bg-gradient {
  @apply bg-gradient-to-br from-slate-900 via-gray-900 to-slate-800 min-h-screen flex items-center justify-center p-4 text-white;
}
```
