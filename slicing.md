# Ejercicio: partir una épica en slices verticales

## La épica

> Como usuario de la billetera, quiero enviar dinero a otro usuario de la app para pagarle
> sin usar efectivo.

Así como está, es una épica gorda: no se puede estimar, no se puede terminar en una
iteración, y esconde decisiones que nadie tomó todavía.

## Parte A — Fragmentar (grupal, 40 min)

Partan la épica en entre 5 y 8 historias VERTICALES.

Vertical significa que cada historia, sola, entrega algo usable de punta a punta.
"Diseñar la pantalla de envío" NO es vertical (es una capa). "Enviar dinero a un contacto
de la agenda con saldo suficiente" SÍ lo es.

Para cada historia escriban: título, formato Como/Quiero/Para, y dos criterios de
aceptación.

_Completar acá, una entrada por historia:_

### Historia 1: [título]

**Como** ...
**Quiero** ...
**Para** ...

Criterios de aceptación:
1. ...
2. ...

## Parte B — Los caminos que no salen bien (grupal, 30 min)

Elijan UNA de sus historias de la Parte A y respondan por escrito:

- ¿Qué pasa si el saldo es insuficiente?
- ¿Qué pasa si el destinatario no existe o está dado de baja?
- ¿Qué pasa si el sistema descuenta el saldo y falla antes de acreditarlo del otro lado?
- ¿Qué pasa si el usuario aprieta "Enviar" dos veces?
- ¿Qué pasa si se cae la conexión justo después de confirmar?

Las últimas tres son las importantes. Anoten qué debería hacer el sistema en cada caso, y
quién tendría que decidirlo (¿el analista? ¿el negocio? ¿el área técnica?).

_Completar acá, una respuesta por pregunta, indicando qué hace el sistema y quién decide._

## Parte C — Defensa (plenario, 30 min)

Cada grupo presenta su corte. Los demás tienen que buscar al menos una historia que NO sea
vertical y justificar por qué. Esta parte se hace oral, en clase — no se documenta en este
archivo.

## Entrega

Este archivo, en la raíz del repositorio del grupo, con las Partes A y B completas.
