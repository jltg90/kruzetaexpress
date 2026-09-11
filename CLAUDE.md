# CLAUDE.md

## Protocolo de tracking (plataforma Cuadra)

> Agregado el 2026-08-04, cuando la fuente de verdad del avance pasó de
> `status.json` a la plataforma.

- ⚠️ La fuente de verdad del avance es la **plataforma Cuadra** (tabla
  `proyectos` en Convex), NO `status.json`. Este repo conserva su
  `status.json` como espejo legible en git — actualízalo igual — pero el dato
  que cuenta es el que reportas.
- Al cerrar cada sesión: actualiza `status.json` y luego corre
  `node scripts/actualizar-estado.mjs`. Si falla por falta de `CUADRA_URL` /
  `CUADRA_TOKEN`, avísale al dueño: sin ese reporte el dashboard central queda
  desactualizado.
- Estados válidos para módulos: `pendiente`, `en_progreso`, `completado`,
  `no_aplica`.
- Estados válidos para `estado_general`: `propuesta`, `en_desarrollo`,
  `en_revision`, `entregado`, `mantenimiento`, `pausado`.
- Mantén el JSON válido siempre.

<!-- stack-por-defecto:inicio v2026-09-11 -->
## Stack por defecto (Cuadra Works)

> Regla del dueño (2026-09-11). Texto completo: `docs/stack-por-defecto.md` en el repo `cuadra`.

- **Punto de partida obligatorio:** Next.js (App Router) + TypeScript + Tailwind v4 en **Vercel**;
  base de datos y funciones en **Convex**; **Clerk** cuando hay varios usuarios con roles (sin
  inventar logins propios); **Resend** para correo; **Vitest** para la lógica pura y
  **Playwright** para recorridos con capturas; publicar solo con `npm run publicar`.
- **Desviarse se puede, pero por escrito antes de construir:** una sección "Desviación del
  stack" en el spec con (1) qué cambia, (2) por qué el stack por defecto NO alcanza para este
  caso, (3) qué cuesta al mes, cuentas nuevas, mantenimiento y respaldos, (4) cómo se volvería.
  Sin esa nota no se desvía; con ella decide el dueño.
- Aplica a proyectos y secciones nuevas. Lo que ya corre con otra cosa no se migra por esta regla.
- Al arrancar, dilo: "Voy con el stack por defecto de Cuadra Works" o "Propongo desviarme en X;
  aquí va la nota".
<!-- stack-por-defecto:fin -->
