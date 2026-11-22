---
name: reels-diarios
description: Genera los 3-4 reels del día para tu cuenta de Instagram/TikTok con formatos variados, hook, guion con tiempos, lista de tomas, dónde y cómo grabar, caption con "Comenta X" y si va a feed o trial. Úsala cuando pidas "dame los reels de hoy", "ideas de reels", "guiones para hoy", "qué grabo hoy", o quieras refrescar el análisis de competencia o el pool de trial reels.
---

# Reels diarios

Produce un paquete diario de 3-4 reels listos para grabar, basado en lo que ya
funciona en tu cuenta y en los outliers (videos que rompen su propio promedio)
de tu competencia.

- Tu contexto (perfil, ganadores, competencia, locaciones): `references/contexto.md`
- Banco de formatos y hooks probados: `references/hooks.md`
- Historial para no repetir ideas: `references/log.md` (leer antes, actualizar después)

Si `contexto.md` todavía tiene campos `{…}` sin llenar, antes de generar nada
pregúntale al usuario lo mínimo para llenarlos (nicho, cuenta, 3-6 competidores,
dónde puede grabar) y guárdalo en el archivo.

## Flujo

1. **Leer** `references/contexto.md`, `references/hooks.md` y `references/log.md`.
2. **Refrescar datos** (solo si el usuario lo pide, o si el último refresh del log
   tiene más de 7 días, y solo si hay un navegador disponible con sesión de Instagram):
   - Abrir `instagram.com/{tu_cuenta}/reels/` y leer las vistas de cada reel.
   - Hacer lo mismo con cada competidor de `contexto.md`.
   - Calcular la **mediana** de vistas por cuenta. Outlier = 2x la mediana o más.
     Usa la mediana, no el promedio: un viral no debe mover la base.
   - Leer el caption de los outliers y anotar su hook en `hooks.md`.
   - Ignorar colaboraciones fuera de nicho y fijados viejos.
   - Tus propios reels con 1.5x tu mediana o más entran al pool de trials.
   - Si no hay navegador, trabaja con los datos que ya están en los archivos y dilo.
3. **Elegir la mezcla del día** (3-4 reels, nunca dos del mismo formato):
   - 1-2 × **Formato A "Comenta X"** (el motor de guardados y follows).
   - 1 × formato de **alcance/personalidad** (B, C o D), rotando según el log.
   - Opcional 1 × **trial reel** del pool (mismo video, solo caption nuevo).
4. **Escribir cada reel** con la plantilla de abajo. Temas: herramientas y proyectos
   reales del usuario (los de `contexto.md`). Nunca inventar métricas, estrellas de
   GitHub ni resultados: si falta un dato, márcalo `[VERIFICAR]`.
5. **Actualizar** `references/log.md` con fecha, título, formato y palabra clave.
6. **Entregar** en el chat, en el idioma y tono del usuario.

## Plantilla por reel

```
### Reel N: {título corto} · Formato {A/B/C/D/E} · {feed | trial}
**Objetivo:** guardados / envíos / follows / comentarios
**Hook (0-3 s):** texto en pantalla: "…" · primera frase dicha: "…"
**Guion:**
- 0-3 s  …
- 3-10 s …
- 10-25 s …
- 25-35 s … (CTA: "Comenta {PALABRA} y te lo mando")
**Tomas:** 1) … 2) … 3) …  (A-roll cara / B-roll pantalla / detalle)
**Dónde:** {locación de contexto.md} · **Cómo:** encuadre, luz, audio, duración
**Edición:** subtítulos, cortes cada ~2 s, zoom en palabras clave, música o audio
**Caption:** (primera línea = "Comenta {PALABRA} y te mando …", 3-5 líneas, 3-5 hashtags)
**Recurso a entregar:** qué recibe quien comenta (guía, repo, prompt)
```

## Reglas

- En formato A, la primera línea del caption SIEMPRE es el CTA "Comenta X y te mando…".
- El hook promete un **resultado concreto** ("busca clientes por ti", "edita tus
  videos"), no solo el nombre de una herramienta.
- Nunca un reel sin caption.
- Duración objetivo 25-40 s. Subtítulos siempre.
- Si un reel necesita un recurso (guía, repo, prompts), di qué preparar antes de
  publicar y recuerda activar el DM automático (ManyChat u otro) para ese post.
- Trials: video idéntico, export nuevo, caption nuevo. Nunca trial de contenido que
  no haya funcionado antes en el feed. Un trial es un post nuevo: necesita su propia
  automatización de DM.
- Respeta las reglas personales que el usuario anote en `contexto.md` (temas que no
  quiere tocar, productos que no se regalan, etc.).
