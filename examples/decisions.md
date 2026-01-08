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

---

## Ejemplo 5: ¿Debo agregar feature que pidió un usuario?

**Contexto:** Un usuario pidió dark mode en la app.

**Aplicando el framework:**

1. ¿Cuántos usuarios lo piden? → 1
2. ¿Es usuario pagante? → NO, free tier
3. ¿Bloquea conversión a pago? → NO

**Decisión:** P2 o NUNCA - Depende de si hay muchos más pidiendo lo mismo

**Principio aplicado:** "10 usuarios que AMAN > 1000 que 'kinda like it'"

---

## Ejemplo 6: ¿Debo migrar la base de datos?

**Contexto:** PostgreSQL funciona bien pero "MongoDB sería más flexible".

**Aplicando el framework:**

1. ¿Está funcionando? → SÍ
2. ¿Hay problemas de performance? → NO
3. ¿Bloquea features críticas? → NO

**Decisión:** NUNCA - "Reescribir lo que funciona: NUNCA"

**Principio aplicado:** Patrick Collison - "Stripe empezó con Ruby + MongoDB. Código feo que funciona > elegante que no existe"
