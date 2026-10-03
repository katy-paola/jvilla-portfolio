# Portfolio · Entrenador deportivo

Sitio web de una sola página (scroll) para un entrenador deportivo. Perfil profesional + presentación personal, con tono cercano y exigente a la vez.

**Stack:** [Astro](https://astro.build) (estático) + [Tailwind CSS v4](https://tailwindcss.com) · sin frameworks de UI · JavaScript mínimo (menú móvil, scroll-spy y revelado de secciones).

## Comandos

| Command     | Action                                          |
| :---------- | :---------------------------------------------- |
| `npm install` | Instala dependencias                          |
| `npm run dev` | Servidor local en `localhost:4321`             |
| `npm run build` | Genera el sitio estático en `./dist/`        |
| `npm run preview` | Vista previa del build                      |

## Estructura

```text
/
├── public/
│   └── jvilla-logo.svg        # logo (también favicon), usado por components/Logo.astro
├── src/
│   ├── styles/global.css      # tokens: color de acento, tipografías, base
│   ├── layouts/Layout.astro   # <head>, SEO, fuentes, script de revelado
│   ├── components/            # una pieza por sección del one-page
│   └── pages/index.astro      # única página: ensambla las secciones
└── astro.config.mjs
```

## Antes de publicar: rellenar los placeholders

Todas las marcas `[...]` están pendientes de datos reales. **No se ha inventado** ningún dato (años exactos, certificaciones, testimonios ni resultados). El nombre ya está rellenado: Jesús Villadiego.

| Qué buscar | Dónde está |
| :--- | :--- |
| `[Tu foto aquí]` | `Hero.astro` — sustituye el bloque con borde discontinuo por `<img>` (ideal: imagen en `src/assets/` con `astro:assets`) |
| Rasgos de "Cómo soy" | `SobreMi.astro` — ajustar si el entrenador pide cambiar alguno |
| `+57 [número]`, `@[usuario]` | `Contacto.astro` — valor visible y `href` del enlace |
| Experiencia exacta / datos profesionales | `Hero.astro` (fila de datos) y `SobreMi.astro` — solo si se proporcionan |

## Diseño

- **Fondo oscuro** (`neutral/zinc-950`) + **acento coral** `#ff6f61` → se cambia en un sitio: `src/styles/global.css` (`--color-accent`).
- **Tipografías:** Sora (títulos) e Inter (texto) — cargadas desde Google Fonts en `Layout.astro`.
- Las animaciones de aparición respetan `prefers-reduced-motion` y tienen fallback sin JavaScript.

## Contenido (español)

Secciones (7): Hero · Valores · Sobre mí (perfil + "Cómo soy") · Cómo trabajo · Servicios · Qué puedes esperar · Contacto.

Convención de tono: **profesionalismo + personalidad, exigencia + cercanía**. Evitar estética de "fitness extremo", frases motivacionales genéricas y promesas de resultados.
