# Curso React: De cero a experto

## Git-Hub: Clonar proyecto.

**git@github-renato:renato-quintupil/udemy-fh-react-CeroAExperto.git**

## Sección 9: Profundizando Hooks

## 116. Inicio de aplicación - HooksApp

### Project: **04-hooks-app**

#### I.- Inicio Proyecto

1. Ejecutar en CLI:

```bash
npm create vite@latest
```

2. Project name: **04-hooks-app**

3. Select framework: **React**

4. Select a variant: **TypeScript + SWC**

   **En versión actualizada de Vite ahora la opción es:**

```
TypeScript + React Compiler
```

5. ir **04-hooks-app/**

```
cd 04-hooks-app/
```

6. Instalar

```bash
npm install
```

7. Iniciar servidor

```bash
npm run dev
```

8. Limpiar proyecto base

9. Crear componente HooksApp.tsx

## 117. TailwindCSS y Estilos

### Instalar y configurar Tailwindcss

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

```
https://gist.github.com/Klerith/8a5440ab34058b22e4874e01e7e931a0
```

Copiar contenido y pegar en **index.css**

```bash
@import "tailwindcss";

.bg-gradient {
  @apply bg-gradient-to-br from-slate-900 via-gray-900 to-slate-800 min-h-screen flex items-center justify-center p-4 text-white;
}
```

Error

```bash
The class bg-gradient-to-br can be written as bg-linear-to-br(suggestCanonicalClasses) .bg-gradient-to-br { --tw-gradient-position: to bottom right in oklab; background-image: linear-gradient(var(--tw-gradient-stops)); }"
```

Solución: Ese warning de VS Code no es un error de CSS. Es una sugerencia del plugin de Tailwind para usar la clase canónica más nueva.

En tu caso:

- **bg-gradient-to-br**
- se puede escribir como
- **bg-linear-to-br**

5. Crear archivo **src/HooksApp.tsx**

6. Agregar estilo al Hola Mundo

```bash
    <div className="bg-gradient">
      <h1 className="text-3xl font-bold underline">Hola Mundo!!!</h1>
    </div>
```

## 118. useState - Estado que re-dibuja

1. Estructura TrafficLight.tsx

Copiar y pegar contenido TrafficLight.tsx

```
https://gist.github.com/Klerith/5bb4c217f7d253a4041ecda7f125254f
```

```bash


export const TrafficLight = () => {


  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-900 via-gray-900 to-slate-800 flex items-center justify-center p-4">
      <div className="flex flex-col items-center space-y-8">
        <div className="w-32 h-32 bg-red-500 rounded-full"></div>
        <div className="w-32 h-32 bg-yellow-500 rounded-full"></div>
        <div className="w-32 h-32 bg-green-500 rounded-full"></div>

        {/* Botón para cambiar el estado de la luz */}
        <div className="flex gap-2">
          <button
            className="bg-red-500 text-white px-4 py-2 rounded-md cursor-pointer">
            Rojo
          </button>
          <button
            className="bg-yellow-500 text-white px-4 py-2 rounded-md cursor-pointer">
            Amarillo
          </button>
          <button
            className="bg-green-500 text-white px-4 py-2 rounded-md cursor-pointer">
            Verde
          </button>
        </div>
      </div>
    </div>
  );
};
```

## 120. useEffect - Disparar efectos secundarios

1. Crear carpeta **02-useEffect**
2. Copiar y pegar archivo **TrafficLightColor.tsx** en carpeta **02-useEffect**
3. Renombrar archivo **./02-useEffect/TrafficLight.tsx** por **TrafficLightWithEffect.tsx**
4. Implement useEffect

## 122. Tarea - CustomHook

1. Copiar y pegar archivo **TrafficLightWithEffect.tsx** en la misma carpeta **02-useEffect**

2. Renombrar archivo **TrafficLightWithEffect copy.tsx** por **TrafficLightWithHook.tsx**

3. Crear carpeta **hooks** en la raiz **/src**

4. Crear archivo **./hooks/useTrafficLight.ts**

## 124. Conectar varios CustomHook entre si

1. Crear carpeta en la raiz **/src/03-examples**
2. Crear archivo **/src/PokemonPage.tsx**
3. Copiar contenido base de PokemonPage desde gist y pegar en **PokemonPage.tsx**

```
https://gist.github.com/Klerith/8ddc0ae428867ee48b2bafd812148d71
```

4. Crear archivo **/hooks/usePokemon.ts**

5. Crear archivo **/hooks/useCounter.ts**

## 126. useRef - Valor que no dispara re-render

1. Crear carpeta en la raiz **/src/04-useRef/**
2. Crear archivo **/src/04-useRef/FocusScreen.tsx**
