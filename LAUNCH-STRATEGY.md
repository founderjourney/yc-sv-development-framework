# YC/SV Development Framework - Estrategia de Lanzamiento

> Objetivo: Publicar el skill de forma que Anthropic lo comparta y sea incluido en repos "awesome"

---

## RESUMEN EJECUTIVO

| Capa | Acción | Objetivo |
|------|--------|----------|
| 1 | Post LinkedIn | Engagement + Autoridad |
| 2 | Repo GitHub | Credibilidad + Descubrimiento |
| 3 | Outreach | Anthropic + Repos Awesome |

---

## CAPA 1: POST DE LINKEDIN

### Timing Óptimo

- **Día:** Martes o Miércoles
- **Hora:** 8-10 AM EST (cuando US tech está despertando)

### El Post (Copiar y Pegar)

```
Pasé 3 horas leyendo TODOS los essays de Paul Graham, Sam Altman, Michael Seibel, Patrick Collison y Brian Chesky.

Luego le pedí a Claude que sintetizara todo en un skill reutilizable.

El resultado: un framework de decisiones para desarrollo que responde la única pregunta que importa:

"¿Esto ayuda a que el próximo cliente pague?"

---

Lo que aprendí destilando 50+ años de sabiduría YC/SV:

1. "Launch something bad quickly" - Michael Seibel
   → Tu primera versión DEBE ser embarrassing

2. "Validation > Architectural purity" - Patrick Collison
   → Stripe empezó con Ruby + MongoDB. Código feo que funciona > elegante que no existe

3. "Do it until it hurts, then automate" - Brian Chesky
   → Manual está BIEN. No automatices lo que no duele

4. "Default alive or default dead" - Paul Graham
   → Si no llegas a rentabilidad antes de quedarte sin dinero, nada más importa

5. "Better to decide and be wrong than equivocate" - Sam Altman
   → La indecisión mata más startups que las malas decisiones

---

El skill completo tiene:
• Framework de decisiones (4 preguntas clave)
• Sistema P0/P1/P2/NUNCA de priorización
• Cuándo aceptar vs pagar vs ignorar deuda técnica
• Decisiones rápidas: tests, refactor, CI/CD, dependencias

Lo hice open source porque creo que cada developer debería tener un "senior advisor de YC" en su terminal.

Link en comentarios.

---

¿Cuál de estos principios contradice más lo que te enseñaron en la universidad?
```

### Hashtags (Primer Comentario, NO en el post)

```
#YCombinator #StartupAdvice #SoftwareEngineering #TechnicalDecisions #BuildInPublic #PaulGraham #ClaudeAI #DeveloperTools #ProductManagement #TechDebt
```

### Por Qué Este Formato Funciona

```yaml
linkedin_algorithm:
  - Hook en primeras 2 líneas: CRÍTICO (el "see more" es tu enemigo)
  - Longitud óptima: 1,200-1,500 caracteres
  - Engagement triggers: pregunta al final, controversial opening
  - Compartibilidad: contenido que hace quedar bien a quien comparte

para_anthropic:
  - Demostrar uso avanzado de Claude (no básico)
  - Crear valor para la comunidad (no solo self-promo)
  - Building in public (ellos aman esto)
  - Citar fuentes originales (rigor)
```

---

## CAPA 2: REPOSITORIO GITHUB

### Estructura del Repo

```
yc-sv-development-framework/
├── README.md              # Showcase del skill
├── SKILL.md               # El skill mismo
├── LICENSE                # MIT (para máxima adopción)
├── examples/
│   └── decisions.md       # Ejemplos de uso real
└── sources.md             # Links a essays originales
```

### README.md (Copiar y Pegar)

```markdown
# YC/SV Development Framework

> Un Claude Skill que sintetiza 50+ años de sabiduría de Y Combinator y Silicon Valley en un framework de decisiones para desarrollo.

## ¿Qué es esto?

Un skill para Claude Code que actúa como un "senior advisor de YC" en tu terminal. Toma decisiones de desarrollo basadas en principios reales de:

- **Paul Graham** - YC Co-founder
- **Sam Altman** - ex-YC President, OpenAI CEO
- **Michael Seibel** - YC CEO
- **Patrick Collison** - Stripe CEO
- **Brian Chesky** - Airbnb CEO

## La Pregunta Central

Antes de cualquier decisión técnica:

> "¿Esto ayuda a que el próximo cliente pague?"

Si la respuesta no es claramente SÍ, probablemente no deberías hacerlo.

## Principios Core

| Principio | Fuente | Implicación |
|-----------|--------|-------------|
| Ship > Perfect | Michael Seibel | "Launch something bad quickly" |
| Validation > Architecture | Patrick Collison | Stripe empezó con Ruby + MongoDB |
| Do Things That Don't Scale | Paul Graham | Manual primero, automatizar cuando duela |
| Default Alive | Paul Graham | Si no llegas a rentabilidad, nada más importa |
| Founder Mode | Brian Chesky | Estar en los detalles NO es micromanagement |

## Instalación

\`\`\`bash
# Copiar SKILL.md a tu directorio de skills de Claude
cp SKILL.md ~/.claude/skills/yc-sv-development-framework/
\`\`\`

## Uso

El skill se activa automáticamente cuando trabajas en:
- Desarrollo de features
- Decisiones de arquitectura
- Priorización de trabajo
- Evaluación de deuda técnica

## Framework de Decisiones

### Pregunta 1: ¿Está funcionando actualmente?
```
SI funciona → NO LO TOQUES
```

### Pregunta 2: ¿Hay usuarios/clientes quejándose?
```
NO hay quejas → No es prioridad
SI hay quejas → Evaluar impacto en revenue
```

### Pregunta 3: ¿Bloquea revenue?
```
SI bloquea revenue → P0 (hacer HOY)
NO bloquea revenue → P1 o P2
```

### Pregunta 4: ¿Cuántos usuarios afecta?
```
10 usuarios que AMAN el producto > 1000 que "kinda like it"
```

## Prioridades

| Nivel | Cuándo | Ejemplos |
|-------|--------|----------|
| **P0** | HOY | Bug que pierde dinero, sistema caído, vulnerabilidad |
| **P1** | Esta semana | Bug de cliente pagante, feature solicitada |
| **P2** | Cuando haya tiempo | Refactoring, tests, documentación |
| **NUNCA** | No hacer | Reescribir lo que funciona, features no solicitadas |

## Fuentes Originales

- [Do Things That Don't Scale](https://paulgraham.com/ds.html) - Paul Graham
- [Startup Advice](https://blog.samaltman.com/startup-advice) - Sam Altman
- [YC's Essential Startup Advice](https://www.michaelseibel.com/blog/yc-s-essential-startup-advice) - Michael Seibel
- [Founder Mode](https://paulgraham.com/foundermode.html) - Paul Graham (sobre Brian Chesky)
- [Stripe Engineering Culture](https://newsletter.pragmaticengineer.com/p/stripe-part-2) - Gergely Orosz

## Contribuir

PRs bienvenidos. El skill debe mantenerse:
- **Conciso** - No agregar por agregar
- **Basado en fuentes reales** - Citar siempre
- **Actionable** - No teoría abstracta

## Licencia

MIT - Úsalo, modifícalo, compártelo.

---

**Creado con [Claude Code](https://claude.ai/code)** | [LinkedIn](https://linkedin.com/in/TU-USUARIO)
```

### LICENSE (MIT)

```
MIT License

Copyright (c) 2026 [Tu Nombre]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### examples/decisions.md

```markdown
# Ejemplos de Decisiones con el Framework YC/SV

## Ejemplo 1: ¿Debo agregar tests?

**Contexto:** Tengo una función de checkout que procesa pagos con Stripe.

**Aplicando el framework:**

1. ¿Está funcionando? → SÍ, pero sin tests
2. ¿Hay quejas? → NO, pero si falla perdemos dinero
3. ¿Bloquea revenue? → Un bug aquí SÍ bloquearía revenue

**Decisión:** P0 - Agregar tests al código de pagos HOY

**Principio aplicado:** "Tests para código crítico de pagos: SÍ"

---

## Ejemplo 2: ¿Debo refactorizar este componente?

**Contexto:** Un componente React de 500 líneas que "se ve feo" pero funciona.

**Aplicando el framework:**

1. ¿Está funcionando? → SÍ
2. ¿Hay quejas? → NO
3. ¿Bloquea revenue? → NO

**Decisión:** NUNCA - No tocar

**Principio aplicado:** "Si 'se ve feo' pero funciona: NO refactorizar"

---

## Ejemplo 3: ¿Debo automatizar el deploy?

**Contexto:** Deploy manual toma 45 minutos, hacemos 3 deploys/semana.

**Aplicando el framework:**

1. ¿Está funcionando? → SÍ, pero lento
2. ¿Hay quejas? → El equipo pierde 2+ horas/semana
3. ¿Bloquea revenue? → NO directamente, pero reduce velocidad de shipping

**Decisión:** P1 - Esta semana, porque "ship fast" es core

**Principio aplicado:** "Si deploy manual toma >30min: SÍ automatizar"

---

## Ejemplo 4: ¿Debo usar este nuevo framework?

**Contexto:** Vi un framework nuevo en Twitter que parece cool.

**Aplicando el framework:**

1. ¿Resuelve problema real HOY? → NO, solo "sería útil"
2. ¿El equipo lo conoce? → NO
3. ¿El actual funciona? → SÍ

**Decisión:** NUNCA - "Sería útil en el futuro: NO"

**Principio aplicado:** "Don't solve problems you don't have" - Paul Graham
```

### sources.md

```markdown
# Fuentes Originales del Framework

## Paul Graham (YC Co-founder)

- [Do Things That Don't Scale](https://paulgraham.com/ds.html) - El essay clásico
- [Founder Mode](https://paulgraham.com/foundermode.html) - Sobre Brian Chesky y Airbnb
- [Default Alive or Default Dead](https://paulgraham.com/aord.html) - La pregunta crítica
- [Startup = Growth](https://paulgraham.com/growth.html) - Definición de startup
- [How to Get Startup Ideas](https://paulgraham.com/startupideas.html) - Make something people want

## Sam Altman (ex-YC President)

- [Startup Advice](https://blog.samaltman.com/startup-advice) - Consejos compilados
- [Startup Advice, Briefly](https://blog.samaltman.com/startup-advice-briefly) - Versión corta
- [Startup Playbook](https://playbook.samaltman.com/) - El playbook completo

## Michael Seibel (YC CEO)

- [YC's Essential Startup Advice](https://www.michaelseibel.com/blog/yc-s-essential-startup-advice) - Lo esencial
- [The Goals of a Pre-Launch Startup](https://www.startuparchive.org/p/former-yc-ceo-michael-seibel-explains-the-goals-of-a-pre-launch-startup) - Pre-lanzamiento

## Patrick Collison (Stripe CEO)

- [Stripe Engineering Culture](https://newsletter.pragmaticengineer.com/p/stripe-part-2) - Gergely Orosz
- [Patrick Collison on Early Stage Startup Principles](https://www.unicorngrowth.io/p/patrick-collison-stripe-startup-principles)

## Brian Chesky (Airbnb CEO)

- [Founder Mode Talk at YC](https://dannydenhard.com/blog/founder-mode-explained) - El talk original
- ["Do it until it hurts, then automate"](https://sketchplanations.com/do-things-that-dont-scale) - La frase célebre

---

## Lecturas Adicionales Recomendadas

- [The Pragmatic Engineer Newsletter](https://newsletter.pragmaticengineer.com/) - Gergely Orosz
- [Y Combinator Library](https://www.ycombinator.com/library) - Recursos oficiales YC
- [Hacker News](https://news.ycombinator.com/) - Comunidad YC
```

---

## CAPA 3: OUTREACH ESTRATÉGICO

### Para Anthropic

#### Opción A - Twitter/X (Más probable que vean)

```
.@AnthropicAI I built a Claude Skill that synthesizes 50+ years of YC/SV wisdom from @paulg, @sama, @maboroshi, @patrickc, and @bchesky into a development decision framework.

Every technical decision now passes through "Will this help the next customer pay?"

Open source: [LINK AL REPO]
```

#### Opción B - Email

**Para:** developer-relations@anthropic.com (o similar)

**Subject:** Open Source Claude Skill - YC/SV Development Framework

**Body:**
```
Hi,

I created an open source Claude Skill that synthesizes development decision-making principles from Y Combinator founders (Paul Graham, Sam Altman, Michael Seibel) and Silicon Valley leaders (Patrick Collison, Brian Chesky).

The skill helps developers make technical decisions by asking: "Will this help the next customer pay?"

It includes:
- Decision framework (4 key questions)
- P0/P1/P2/NEVER prioritization system
- Technical debt guidelines
- Quick decisions for tests, refactoring, CI/CD

GitHub: [LINK]
LinkedIn post: [LINK]

Would love any feedback, and happy to contribute to official skill repositories if there's interest.

Best,
[Tu nombre]
```

### Para Repos "Awesome"

1. **awesome-claude** (si existe)
2. **awesome-ai-tools**
3. **awesome-developer-tools**
4. **awesome-chatgpt** (muchos aceptan Claude también)

**Template de PR:**

```markdown
## Add YC/SV Development Framework Skill

**What:** A Claude Skill that synthesizes development decision-making principles from YC founders and SV leaders.

**Why:** Helps developers make technical decisions using proven frameworks from Paul Graham, Sam Altman, Michael Seibel, Patrick Collison, and Brian Chesky.

**Link:** [GitHub repo]

**Category suggestion:** AI Development Tools / Decision Frameworks
```

---

## CHECKLIST DE EJECUCIÓN

### PRE-LAUNCH

- [ ] Crear repo GitHub público
- [ ] Copiar README.md a repo
- [ ] Copiar SKILL.md a repo
- [ ] Agregar LICENSE (MIT)
- [ ] Crear carpeta examples/ con decisions.md
- [ ] Crear sources.md con links
- [ ] Verificar todos los links funcionan
- [ ] Agregar tu LinkedIn al README

### LAUNCH DAY

- [ ] Publicar en LinkedIn (Martes/Miércoles 8-10 AM EST)
- [ ] Poner link del repo en PRIMER comentario
- [ ] Responder TODOS los comentarios en primera hora (engagement crítico)
- [ ] Publicar en Twitter mencionando @AnthropicAI
- [ ] Compartir en comunidades relevantes:
  - [ ] Hacker News (si tienes karma suficiente)
  - [ ] Reddit r/ClaudeAI
  - [ ] Reddit r/startups
  - [ ] Discord de Claude (si existe)

### POST-LAUNCH (48 horas después)

- [ ] Enviar PRs a repos "awesome-*"
- [ ] Enviar email a Anthropic Developer Relations
- [ ] Documentar métricas (likes, comments, shares, stars)
- [ ] Screenshot del engagement para siguiente post
- [ ] Iterar basado en feedback

---

## FACTOR CLAVE PARA QUE ANTHROPIC COMPARTA

Lo que hace que Anthropic comparta algo:

| Factor | Tu Skill |
|--------|----------|
| Demuestra capacidad avanzada de Claude | ✅ Skill creation es avanzado |
| Crea valor para la comunidad | ✅ Open source, útil |
| Building in public | ✅ LinkedIn post documenta proceso |
| Rigor | ✅ Citas reales, fuentes verificables |
| No es cringe | ✅ Sin hype exagerado |
| Bien documentado | ✅ README, examples, sources |

---

## NOTAS FINALES

### El post funciona porque:

1. **Hook irresistible** - "Pasé 3 horas leyendo..." genera curiosidad
2. **Name dropping estratégico** - Paul Graham, Sam Altman son reconocidos
3. **Valor inmediato** - Los 5 principios son útiles sin necesidad del skill
4. **CTA claro** - Link en comentarios
5. **Pregunta de engagement** - Invita a comentar

### El repo funciona porque:

1. **README scannable** - Tabla de principios visible inmediatamente
2. **Instalación simple** - Una línea
3. **Ejemplos concretos** - decisions.md muestra uso real
4. **Fuentes verificables** - sources.md da credibilidad
5. **MIT license** - Máxima adopción

---

**Archivo creado:** 2026-01-08
**Ubicación:** ~/.claude/skills/yc-sv-development-framework/LAUNCH-STRATEGY.md
