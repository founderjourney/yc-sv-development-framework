---
name: yc-sv-development-framework
description: |
  Framework de decision-making para desarrollo de software estilo Y Combinator / Silicon Valley.
  Basado en principios reales de Paul Graham, Sam Altman, Michael Seibel, Patrick Collison y Brian Chesky.

  Usar cuando:
  - Desarrollando features o productos
  - Tomando decisiones tecnicas (que hacer, como, cuando)
  - Priorizando trabajo (P0, P1, P2)
  - Evaluando si refactorizar o parchar
  - Decidiendo sobre deuda tecnica
  - Evaluando si agregar tests, CI/CD, o automatizacion
  - Cualquier decision de arquitectura o ingenieria

  Triggers: desarrollo, codigo, feature, refactor, arquitectura, priorizar, decision tecnica,
  que hacer primero, deuda tecnica, tests, CI/CD, sprint, backlog
---

# YC/SV Development Framework

Framework de decision-making basado en principios de fundadores de Y Combinator y Silicon Valley.

## LA PREGUNTA CENTRAL

Antes de cualquier decision tecnica, preguntar:

> "Will this make the boat go faster?" (Jony Ive via Brian Chesky)
> "Does this help us make something people want?" (Paul Graham, YC motto)

Si la respuesta no es claramente SI, probablemente no deberias hacerlo.

---

## PRINCIPIOS CORE

### 1. Ship > Perfect (Michael Seibel)

```
"Launch something bad quickly" - Michael Seibel, YC CEO
"If you walk away with one thing: launch something bad quickly"
```

- Lanzar MVP en dias, no semanas
- Iterar basado en feedback real
- La primera version DEBE ser embarrassing

### 2. Validation > Architecture (Patrick Collison)

```
"Validation trumps architectural purity" - Stripe fue construido en Ruby con MongoDB
```

- Codigo feo que funciona > codigo elegante que no existe
- No optimizar prematuramente
- Resolver el problema primero, refactorizar despues (si es necesario)

### 3. Do Things That Don't Scale (Paul Graham)

```
"Do it until it hurts, then automate it away" - Brian Chesky
```

- Procesos manuales estan BIEN al inicio
- No automatizar hasta que el proceso manual sea un bottleneck real
- Usar "Collison installation": configurar clientes manualmente uno por uno

### 4. Default Alive or Dead (Paul Graham)

```
Preguntarte: "Si no levanto mas dinero, llegare a rentabilidad antes de quedarme sin runway?"
```

- Si eres "default dead", NADA importa excepto cambiar eso
- Features fancy son irrelevantes si el negocio muere

### 5. Founder Mode (Brian Chesky)

```
"Be in the details. Great leadership is presence, not absence"
"You don't manage people. You manage people through the work" - Jony Ive
```

- Estar en los detalles NO es micromanagement
- Conocer el codigo, el producto, los clientes

---

## FRAMEWORK DE DECISIONES

### Pregunta 1: Esta funcionando actualmente?

```
SI funciona → NO LO TOQUES
"If it works, don't touch it"
```

### Pregunta 2: Hay usuarios/clientes quejandose?

```
NO hay quejas → No es prioridad
SI hay quejas → Evaluar impacto en revenue
```

### Pregunta 3: Bloquea revenue?

```
SI bloquea revenue → P0 (hacer HOY)
NO bloquea revenue → P1 o P2
```

### Pregunta 4: Cuantos usuarios afecta?

```
10 usuarios que AMAN el producto > 1000 que "kinda like it"
- Michael Seibel
```

---

## PRIORIDADES (P0/P1/P2)

### P0 - Hacer HOY
- Bug que pierde dinero/clientes
- Sistema caido
- Vulnerabilidad de seguridad explotable
- Feature que bloquea primer pago

### P1 - Esta semana
- Bug reportado por cliente pagante
- Feature solicitada por multiples clientes
- Deuda tecnica causando bugs recurrentes

### P2 - Cuando haya tiempo
- Refactoring "para limpiar"
- Tests para codigo que funciona
- CI/CD improvements
- Documentacion

### NUNCA
- Reescribir algo que funciona
- Agregar features que nadie pidio
- "Mejoras" sin problema real que resolver

---

## DEUDA TECNICA

### Cuando ACEPTAR deuda tecnica

```
"Tech debt is leverage - most startups need it" - YC
```

- Para lanzar mas rapido
- Para validar hipotesis
- Cuando el costo de NO tenerla es mayor que el interes

### Cuando PAGAR deuda tecnica

- Cuando se convierte en bottleneck para nuevas features
- Cuando causa bugs recurrentes (alto "interes")
- Cuando el 20% del codigo causa 80% del dolor (Pareto)

### Cuando IGNORAR deuda tecnica

- Si el codigo funciona y nadie lo toca
- Si el negocio puede morir antes de que importe
- Si no afecta clientes

---

## DECISIONES TECNICAS RAPIDAS

### Agregar tests?

```
Tests para codigo critico de pagos: SI
Tests para UI que cambia cada semana: NO
Tests despues de bug en produccion: SI
Tests "por buenas practicas": NO
```

### Refactorizar?

```
Si el codigo actual bloquea feature necesaria: SI
Si "se ve feo" pero funciona: NO
Si causa bugs recurrentes: SI
Si "seria mas elegante": NO
```

### Agregar CI/CD?

```
Si deploy manual toma >30min: SI
Si hay <10 deploys/mes: NO
Si errores de deploy son comunes: SI
Si el equipo es 1-2 personas: PROBABLEMENTE NO
```

### Nueva dependencia/framework?

```
Resuelve problema real que tienes HOY: SI
"Seria util en el futuro": NO
Equipo ya lo conoce: BONUS
Nadie lo conoce: CUIDADO
```

---

## COMUNICACION DE DECISIONES

### Con stakeholders no-tecnicos (Sam Altman)

```
"Listen to everyone. Then make your own decision."
"It's better to make a decision and be wrong than to equivocate."
```

1. Escuchar el problema de negocio
2. Proponer solucion tecnica simple
3. Dar timeline realista (y cumplirlo)
4. NO pedir permiso para decisiones tecnicas

### Cuando decir NO

- "Eso requeriria reescribir X, que funciona bien"
- "Podemos hacerlo, pero retrasaria Y que es mas importante"
- "La version simple toma 2 dias, la 'correcta' toma 2 semanas"

---

## METRICAS QUE IMPORTAN

```
"Choose 1-2 key metrics. Decide based nearly exclusively on how tasks impact those metrics"
- Michael Seibel
```

### Para SaaS B2B:
1. MRR (Monthly Recurring Revenue)
2. Churn rate

### Para Marketplace:
1. GMV (Gross Merchandise Value)
2. Take rate

### Para Consumer:
1. DAU/MAU
2. Retention D7/D30

### NO medir:
- Lineas de codigo
- Test coverage (excepto como senal)
- "Velocidad" del equipo
- Story points

---

## RESUMEN EJECUTIVO

```yaml
hacer:
  - Lanzar rapido, iterar basado en datos
  - Resolver problemas reales de usuarios reales
  - Codigo feo que funciona > codigo elegante que no existe
  - Manual primero, automatizar cuando duela

no_hacer:
  - Refactorizar codigo que funciona
  - Agregar features que nadie pidio
  - Optimizar antes de tener usuarios
  - "Mejores practicas" sin problema real

preguntas_guia:
  - "Esto ayuda a que el proximo cliente pague?"
  - "Cuantos usuarios se quejan de esto?"
  - "Que pasa si NO hacemos esto?"
  - "Cual es la version mas simple que resuelve el problema?"
```

---

## FUENTES

Principios extraidos de:
- Paul Graham (YC Co-founder): paulgraham.com
- Sam Altman (ex-YC President): blog.samaltman.com
- Michael Seibel (YC CEO): michaelseibel.com
- Patrick Collison (Stripe CEO): Entrevistas y cultura de Stripe
- Brian Chesky (Airbnb CEO): "Founder Mode" talk at YC 2024
