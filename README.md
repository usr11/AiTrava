# AiTrava · Landing

Landing page de AiTrava, viajes sorpresa personalizados. Hecha con [Astro](https://astro.build).

## Comandos

| Comando           | Acción                                |
| :---------------- | :------------------------------------ |
| `npm install`     | Instala dependencias                  |
| `npm run dev`     | Servidor local en `localhost:4321`    |
| `npm run build`   | Genera el sitio estático en `./dist/` |
| `npm run preview` | Sirve el build localmente             |

## Estructura

```text
src/
├── assets/            Logo (optimizado con astro:assets)
├── components/        Una sección de la landing por componente
├── data/site.ts       Textos, links, redes y presupuesto de ejemplo
├── layouts/           HTML base, SEO y fuentes
├── pages/index.astro
└── styles/global.css  Tokens de color (docs/desgin.txt) y utilidades
design/                Fuentes del diseño (canvas)
docs/                  Modelo de negocio, paleta y logo
```

Las fuentes (Big Shoulders, Familjen Grotesk, IBM Plex Mono) se descargan en el build y se sirven desde el propio sitio con la API de fuentes de Astro.

## Despliegue

Se despliega en Cloudflare Workers como sitio estático (`wrangler.jsonc` sirve `./dist`). Build: `npm run build`, deploy: `npx wrangler deploy`.

## Pendiente

- Links de App Store y Google Play en `src/data/site.ts` (`stores`).
