# GUIBL Design System

Sistema de diseño **Paradigm-inspired** para apps GUIBL: CSS puro, tokens compartidos, esquinas rectas en UI operativa.

Referencia visual: [Paradigm](https://www.paradigmai.com/)

## Contenido

| Archivo | Descripción |
|---------|-------------|
| [`design-system.html`](design-system.html) | Guía visual interactiva (componentes, tokens, patrones) |
| [`design/guibl-paradigm-tokens.css`](design/guibl-paradigm-tokens.css) | Tokens CSS `--pg-*` para importar en cualquier app |
| [`DESIGN.md`](DESIGN.md) | Documentación de principios y convenciones |
| [`assets/logo_01.svg`](assets/logo_01.svg) | Logo GUIBL |

## Ver la guía

**Opción 1 — archivo local**

Abrí `design-system.html` en el navegador.

**Opción 2 — servidor estático**

```bash
npx serve .
```

Luego entrá a `http://localhost:3000/design-system.html`

## Usar los tokens en tu app

```css
@import url("ruta/al/design/guibl-paradigm-tokens.css");

html[data-theme="light"] {
  /* Listo: --pg-accent, --pg-canvas, --pg-border, etc. */
}
```

Activá el tema claro en el HTML:

```html
<html lang="es" data-theme="light">
```

## Stack compatible

- React + TypeScript + Vite
- CSS puro con variables (sin Tailwind, sin CSS modules)
- Tipografías: [Inter](https://fonts.google.com/specimen/Inter) + [Newsreader](https://fonts.google.com/specimen/Newsreader)

## Licencia

Uso interno GUIBL Studio. Consultá antes de redistribuir fuera del estudio.
