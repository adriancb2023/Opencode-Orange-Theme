# Orange Theme — Opencode

Tema vivo naranja/rojo inspirado en el cerebro holográfico (WezTerm orange). Colores saturados sobre fondo oscuro `#0A0A14`.

## Contenido
- `orange.json` — definición del tema opencode

## Instalación

### Opción 1 — Manual (recomendada)
1. Copia `orange.json` a tu carpeta de temas:
   ```
   C:\Users\Harvie\.config\opencode\themes\orange.json
   ```
   Linux/macOS: `~/.config/opencode/themes/orange.json`

2. Activa el tema en `tui.json`:
   ```json
   {
     "$schema": "https://opencode.ai/tui.json",
     "theme": "orange"
   }
   ```
   Archivo: `C:\Users\Harvie\.config\opencode\tui.json` (o `~/.config/opencode/tui.json`)

3. Reinicia opencode.

### Opción 2 — Esta carpeta ya es un backup
Esta carpeta `orange theme` en el Escritorio es tu backup portable. Para reinstalar en otro PC, repite el paso 1 y 2.

## Vista previa

Simulacion sobre fondo `#0A0A14` / texto `#FFE8D6`:

```typescript
// syntaxKeyword #FF6B9D  | syntaxFunction #2979FF | syntaxString #00E676
import { brain } from "./hologram"; // comment #6B6580

type Hologram = { glow: string }; // syntaxType #FFCA28

function ignite(brain: Hologram): number { // syntaxFunction #2979FF
  const energy = 3.14; // syntaxNumber #FF6B35
  const active = brain.glow === "orange"; // syntaxString #00E676 | syntaxOperator #00E5FF
  return active ? energy : 0;
}
```

Markdown y UI:
- **Headings** en naranja vivo `#FF3B1F`, **links** cyan `#00E5FF`, **code inline** amarillo `#FFCA28`
- Paneles `bgPanel #12111F`, bordes activos `borderActive #FF3B1F` (glow naranja al enfocar)
- Diff: añadido verde `#00E676` sobre `#0F2A1A`, eliminado rojo `#FF1A1A` sobre `#2A0F0F`
- Selección/borde primario siempre naranja — el tema respira holograma, no pastel.

> Tip: abre `orange.json` con la paleta arriba para ver el hex exacto de cada token.

## Paleta
| Token | Color | Uso |
|-------|-------|-----|
| bg | `#0A0A14` | fondo principal |
| bgPanel | `#12111F` | paneles |
| fg | `#FFE8D6` | texto |
| orange / primary | `#FF3B1F` | acento, headings, borde activo |
| orangeGlow / accent | `#FF6B35` | números, highlight |
| amber / warning | `#FFCA28` | tipos, warnings |
| green / success | `#00E676` | strings, diff añadido |
| blue / info | `#2979FF` | funciones, info |
| cyan / operator | `#00E5FF` | operadores, links |
| magenta / keyword | `#FF6B9D` | keywords |

## Desinstalar / Volver atrás
Cambia en `tui.json`:
```json
"theme": "neurobrain2"
```
o borra la línea `theme` para volver al default.

## Requisitos
Opencode >= 0.1 con soporte `theme` en `tui.json` (schema `https://opencode.ai/theme.json`).
