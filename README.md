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

```bash
# Copiar SKILL.md a tu directorio de skills de Claude
cp SKILL.md ~/.claude/skills/yc-sv-development-framework/
```

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

**Creado con [Claude Code](https://claude.ai/code)**
