# 04-hooks-app

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
**https://gist.github.com/Klerith/8a5440ab34058b22e4874e01e7e931a0**

Copiar contenido y pegar en **index.css**

```bash
@import "tailwindcss";

.bg-gradient {
  @apply bg-gradient-to-br from-slate-900 via-gray-900 to-slate-800 min-h-screen flex items-center justify-center p-4 text-white;
}
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
