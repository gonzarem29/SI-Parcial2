# AGENTS.md — SI (Seguridad Industrial)

## Contexto

Repositorio de materiales de estudio para el segundo parcial de **Seguridad Industrial** (UBP). Contiene PDFs y una página de estudio interactiva con estética **Sala de Control Industrial** (SCADA/HMI) — paneles CRT, indicadores LED, barras de progreso y telemetría.

## Archivos

| Archivo | Origen |
|---------|--------|
| `SI-U5.pdf` | U5 — Seguridad de Redes |
| `SI-U5---cloud.pdf` | U5 — Cloud Computing |
| `SIU6---2026.pptx.pdf` | U6 — Ingeniería de Seguridad de Software (PPTX convertido) |
| `WebGoat---Unidad-6.pdf` | U6 — WebGoat |
| `SI-U7-2026.pdf` | U7 — Seguridad de la Información |
| `index.html` | Página de estudio (SCADA / Control Room design) |
| `brandkit.config.yaml` | Configuración BrandKit |
| `brand_atomic_system/` | Sistema de diseño atómico |
| `assets/*.svg` | 6 SVGs generados con Nakkas (hazard-stripe, scanline, grid-bg, telemetry-line, led-dot, frame-corners) |
| `.gitignore` | Exclusiones: `.opencode/`, `screenshots/`, `temp_*`, `package*.json`, `node_modules/` |

## GitHub

| | |
|---|----|
| Repo | `github.com/gonzarem29/SI-Parcial2` |
| Pages | `https://gonzarem29.github.io/SI-Parcial2/` |
| Branch | `main`, deploy desde `/ (root)` |

## MCPs configurados

Ver `.opencode.json`:
- **notebooklm** — NotebookLM MCP para consultar fuentes (autenticado y funcional)
- **markitdown** — Conversión PDF a texto (en desuso, extracción directa con Python)
- **nakkas** — Generación de SVGs (utilizado para assets/*.svg)
- **playwright** — Screenshots/testing (requiere configuración)
- **aesthetics-wiki** — Investigación de diseño (acceso via web search)
- **brandkit** — Gestión de identidad visual (archivos actualizados manualmente)

## Diseño del index.html

- Single HTML con CSS + JS inline
- Estética Sala de Control Industrial (SCADA/HMI)
- Paneles con bisel CRT (bezel dark + inner highlight + scanlines SVG)
- Barra HMI superior con estado del sistema
- Navegación por pestañas industriales con LED indicator
- Hero con display principal estilo monitor de control + frame corners SVG
- 5 unidades con tarjetas tipo monitor panel (LED + barra de progreso + contenido expandible)
- Divisores entre unidades con línea de telemetría (ECG-style) — waveform SVG
- Boot overlay con animación POST industrial y barras de progreso
- Hazard tape decorativa (SVG inline) patrón diagonal amarillo/negro
- Grid background (SVG inline)
- Paleta: fondo `#121212`, verde status `#22c55e`, rojo alerta `#ef4444`, amarillo safety `#eab308`, azul datos `#3b82f6`, cyan `#06b6d4`, orange `#f97316`
- Tipografía: JetBrains Mono (contenido) + Inter (etiquetas/pantallas)
- prefers-reduced-motion, skip-to-content, ARIA labels
- Favicon: shield/panel icon with glowing LED
- Optimizado para iPad Pro 12.9" + monitores 16:9 y 16:10 (desktop-first)

## Estados del proyecto

### Completado
- Health Check: NotebookLM autenticado, 6 MCPs configurados
- Aesthetics Wiki Research: referencias HMI/SCADA/SOC industriales documentadas
- Nakkas SVGs: 6 assets generados e inlineados en HTML (grid bg, hazard tape, scanline, telemetry waveform, led dot, frame corners)
- NotebookLM Content Validation: 5 unidades validadas contra fuentes (contenido correcto y completo)
- BrandKit: palette.css actualizado con --glow-cyan y --glow-orange, HTML :root sincronizado
- Favicon agregado (shield/panel + LED verde)
- Telemetry dividers actualizados con waveform realista
- Frame corners overlay en hero panel
- Timing boot overlay ajustado
- Playwright: 45 screenshots (5 viewports × 9 captures) + 20 tests de interacción
- GitHub: repo creado + push a `main` + Pages configurado

### Pendiente (opcional)
- Pumpking de contenido con detalles adicionales de NotebookLM

## Convenciones

- No usar emojis a menos que el usuario lo pida explícitamente
- Código sin comentarios
- Respetar diseño desktop-first con breakpoints para iPad Pro 12.9"
