---
name: GUIBL Paradigm-Inspired
description: Enterprise research-tool aesthetic for GUIBL apps.
reference: https://www.paradigmai.com/
---

# GUIBL Paradigm-Inspired Design

Referencia visual: [Paradigm](https://www.paradigmai.com/). Herramienta enterprise limpia, neutra y precisa. Prioriza legibilidad, jerarquía tipográfica y densidad controlada.

## Visual Theme

- Canvas gris muy claro (`#f6f7f8`), no verde/oliva.
- Superficies blancas con bordes finos `#e3e4e8`.
- Sin sombras decorativas; la profundidad viene del contraste y el espaciado.
- Acento azul (`#0a33ff`) solo para CTAs, foco y selección activa.
- Radios: **0** en UI operativa (tableros, inputs, botones). Sin píldoras salvo badges puntuales.

## Typography

- **Body / UI**: Inter, 14px, peso 400–500.
- **Títulos**: Newsreader (serif), peso 500–600, line-height 1.15.
- **Labels**: Inter, 11px, uppercase, letter-spacing 0.04em, color muted.
- **KPIs**: Inter, 24px, peso 600.

## Components

### Buttons

Primario: fondo `#0a33ff`, texto blanco, radio 6px — **solo CTAs explícitos** (guardar, crear, enviar).

Secundario: fondo blanco, borde `#e3e4e8`, texto ink.
Ghost: sin borde, hover `#f0f0f2`.

**UI densa (tableros, presupuestos):**

| Control | Fondo | Acento azul |
|---------|-------|-------------|
| Date picker trigger | blanco + borde | solo en `:focus` |
| Iconos copy/delete | transparente | solo en `:hover` |
| Celdas estado (semáforo) | gris / naranja / verde / teal | nunca azul Paradigm |
| Inputs en tabla | blanco + borde | solo ring en `:focus` |

**Anti-patrón:** `html[data-theme="light"] button { background: accent }` — pisa date pickers, iconos y semáforo.

### Cards & Panels

```css
background: #ffffff;
border: 1px solid #e3e4e8;
border-radius: 12px;
box-shadow: none;
```

### Forms

Inputs 36px de alto, radio 6px, focus ring azul sutil.

## Uso de tokens

```css
@import url("./design/guibl-paradigm-tokens.css");

html[data-theme="light"] {
  /* variables --pg-* y alias --bg, --surface, --accent, etc. */
}
```

## Archivos

| Archivo | Descripción |
|---------|-------------|
| `design-system.html` | Guía visual interactiva |
| `design/guibl-paradigm-tokens.css` | Tokens `--pg-*` compartidos |
| `assets/logo_01.svg` | Logo GUIBL |

## Don't

- No usar naranja/amber como acento principal.
- No usar canvas oliva, paneles oscuros de foco ni acentos naranja (estilo descartado).
- No Tailwind ni CSS modules.
