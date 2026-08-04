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
