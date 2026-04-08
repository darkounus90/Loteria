---
name: ui-ux-pro-max
description: Comprehensive design guide for web and mobile applications. Contains 67 styles, 161 color palettes, 57 font pairings, 99 UX guidelines, and 25 chart types across 16 technology stacks. Searchable database with priority-based recommendations.
---

# ui-ux-pro-max

Comprehensive design guide for web and mobile applications. Contains 67 styles, 161 color palettes, 57 font pairings, 99 UX guidelines, and 25 chart types across 16 technology stacks. Searchable database with priority-based recommendations.

## When to Apply

Cuando el trabajo involucra **estructura de UI, decisiones de diseño visual, patrones de interacción o control de calidad de UX**, se debe usar esta Skill.

### Must Use

Es obligatorio llamar a esta Skill en los siguientes casos:

- Diseño de nuevas páginas (Landing Page, Dashboard, Admin, SaaS, Mobile App)
- Creación o reestructuración de componentes de UI (botones, modales, formularios, tablas, gráficas, etc.)
- Elección de esquemas de color, sistemas tipográficos, normas de espaciado o sistemas de diseño
- Revisión de código de UI para UX, accesibilidad o consistencia visual
- Implementación de estructuras de navegación, animaciones o comportamiento responsivo
- Toma de decisiones de diseño a nivel de producto (estilo, jerarquía de información, expresión de marca)
- Mejora de la calidad percibida, claridad o usabilidad de la interfaz

### Recommended

Se recomienda usar esta Skill en los siguientes casos:

- La UI se ve "poco profesional", pero la razón no está clara
- Se recibe feedback sobre usabilidad o experiencia
- Optimización de la calidad de la UI antes del lanzamiento
- Necesidad de alinear el diseño multiplataforma (Web / iOS / Android)
- Construcción de un sistema de diseño o biblioteca de componentes reutilizables

### Skip

No es necesario usar esta Skill en los siguientes casos:

- Desarrollo de lógica puramente backend
- Tareas que solo involucran diseño de API o base de datos
- Optimización de rendimiento no relacionada con la interfaz
- Trabajo de infraestructura o DevOps
- Scripts no visuales o tareas de automatización

**Criterio de decisión**: Si la tarea cambia **cómo se ve, cómo se usa, cómo se mueve o cómo se interactúa** con una función, se debe usar esta Skill.

## Rule Categories by Priority

| Prioridad | Categoría | Impacto | Dominio | Verificaciones Clave (Must Have) | Anti-Patrones (Evitar) |
|----------|----------|--------|--------|------------------------|------------------------|
| 1 | Accesibilidad | CRÍTICO | `ux` | Contraste 4.5:1, texto Alt, naveg. teclado, Aria-labels | Quitar anillos de enfoque, botones de solo icono sin etiquetas |
| 2 | Toque e Interacción | CRÍTICO | `ux` | Tamaño mín. 44×44px, espaciado 8px+, feedback de carga | Confianza solo en hover, cambios de estado instantáneos (0ms) |
| 3 | Rendimiento | ALTO | `ux` | WebP/AVIF, Lazy loading, reserva de espacio (CLS < 0.1) | Layout thrashing, Cumulative Layout Shift |
| 4 | Selección de Estilo | ALTO | `style`, `product` | Coincidencia con tipo de producto, Consistencia, iconos SVG (sin emoji) | Mezclar estilos planos y esqueumórficos al azar, Emoji como iconos |
| 5 | Diseño y Responsivo | ALTO | `ux` | Breakpoints mobile-first, Viewport meta, sin scroll horizontal | Scroll horizontal, anchos de contenedor fijos en px, desactivar zoom |
| 6 | Tipografía y Color | MEDIO | `typography`, `color` | Base 16px, Line-height 1.5, tokens de color semánticos | Texto < 12px, gris sobre gris, hex puros en componentes |
| 7 | Animación | MEDIO | `ux` | Duración 150–300ms, el movimiento transmite significado | Animación solo decorativa, animar width/height, no respetar reduced-motion |
| 8 | Formularios y Feedback | MEDIO | `ux` | Etiquetas visibles, error cerca del campo, texto de ayuda | Etiqueta solo en placeholder, errores solo arriba, abrumar de entrada |
| 9 | Patrones de Navegación | ALTO | `ux` | Regreso predecible, Nav inferior ≤5, Deep linking | Navegación sobrecargada, comportamiento de "atrás" roto, sin deep links |
| 10 | Gráficas y Datos | BAJO | `chart` | Leyendas, Tooltips, colores accesibles | Depender solo del color para transmitir significado |

# Prerequisites

Check if Python is installed:

```bash
python3 --version || python --version
```

If Python is not installed, install it based on user's OS:

**macOS:**
```bash
brew install python3
```

---

## How to Use This Skill

### Step 1: Analyze User Requirements

Extract key information from user request:
- **Product type**: Entertainment, Tool, Productivity, etc.
- **Target audience**: Consumer, Professional, etc.
- **Style keywords**: playful, vibrant, minimal, dark mode, etc.
- **Stack**: HTML + Tailwind (default for this project)

### Step 2: Generate Design System (REQUIRED)

**Always start with `--design-system`** to get comprehensive recommendations with reasoning:

```bash
python3 .agents/skills/ui-ux-pro-max/scripts/search.py "<query>" --design-system [-p "Project Name"]
```

### Step 3: Implement following the guidelines

Use the generated design system and the rules in this skill to build professional UI.

---
