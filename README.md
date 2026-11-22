# 🎬 reels-diarios: una skill de Claude que te escribe los reels del día

Le dices a Claude **"dame los reels de hoy"** y te entrega 3-4 reels listos para grabar:

- **Hook** para los primeros 3 segundos (texto en pantalla + primera frase)
- **Guion** con tiempos
- **Tomas**: cara, pantalla, detalle
- **Dónde y cómo grabarlo**: encuadre, luz, audio, duración
- **Edición** y **caption** con el "Comenta X" en la primera línea
- Si va al **feed** o como **trial reel**

No inventa ideas de la nada. Se basa en **qué videos de tu competencia rompieron su propio promedio** (outliers), les saca el hook y lo adapta a tus proyectos.

*Por Duke · [@dukethropic](https://instagram.com/dukethropic)*

---

## Lo que necesitas

- [Claude Code](https://claude.com/claude-code) (o la app de Claude con skills)
- Opcional: un navegador conectado a Claude con tu sesión de Instagram, para que refresque los datos solo. Sin navegador también funciona con los datos que tú le pongas.

## Instalación

```bash
git clone https://github.com/Dukedanidd/reels-diarios-skill.git
cp -r reels-diarios-skill/reels-diarios ~/.claude/skills/
```

Listo. Abre Claude Code y escribe:

> **dame los reels de hoy**

La primera vez te va a preguntar tu nicho, tu cuenta, 3-6 competidores y dónde puedes grabar. Lo guarda en `references/contexto.md` y de ahí en adelante ya no te pregunta.

## Cómo funciona

```
reels-diarios/
├── SKILL.md                 # instrucciones para Claude
└── references/
    ├── contexto.md          # tu perfil, tus ganadores, tu competencia, tus locaciones
    ├── hooks.md             # banco de formatos y hooks probados
    └── log.md               # lo que ya te dio, para no repetir
```

1. **Lee** tu contexto, el banco de hooks y el log.
2. **Refresca datos** si pasaron más de 7 días: vistas de tus reels y de tu competencia, mediana por cuenta, outliers de 2x o más.
3. **Arma la mezcla**: 1-2 reels "Comenta X", 1 de alcance o personalidad y, opcional, 1 trial con un reel tuyo que ya funcionó.
4. **Escribe** cada reel con la plantilla y **anota** todo en el log.

## Tips

- **Llena bien `contexto.md`.** Entre más real sea (tus proyectos, tus números, tus lugares), mejores guiones.
- **Agrega reglas personales** en `contexto.md`, por ejemplo "no enseñar mi producto de pago".
- **El recurso va primero.** Si un reel dice "Comenta X", ten listo lo que vas a mandar y activa el DM automático antes de publicar.
- **Trials solo con ganadores.** Un trial reel es para distribuir lo que ya funcionó, no para probar ideas nuevas.

---

**¿La usaste?** Mándame captura por DM a **@dukethropic** y te comparto en stories 🔥

Licencia MIT.
