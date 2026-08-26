---
name: mensajes
description: Convierte "no sé qué responder" en 3-5 mensajes listos para copiar y pegar, a partir de una captura de la conversación, del texto pegado, de una nota o estado, o solo de la intención. Trabaja con estilos que se eligen por nombre — sociales (abrir, gracioso, coqueto, provocativo, interés genuino, rescate, cerrar plan, incógnita, cortar con elegancia) y de trabajo (firme y cordial, cobro, mala noticia, decir que no, desescalar, seguimiento) — en español neutro, calibrados al medio (WhatsApp ≠ correo ≠ DM), al registro de la otra persona y al momento. Usar SIEMPRE que aparezca algo como "qué le respondo", "cómo le digo", "no sé qué contestar", "ayúdame a responder esto", "cómo le cobro sin sonar pesado", "cómo le digo que no", "suaviza este mensaje", "hazlo menos seco", "me escribió enojado", "se murió la conversación", "cómo le propongo salir", "quiero dejarle la incógnita", "qué le pongo a esta nota / estado / historia" — y también cuando el usuario simplemente pegue o adjunte una captura de un chat, un DM o un correo esperando ayuda para contestar, aunque no pida nada explícitamente. NO usar para textos largos (artículos, posts, documentación, propuestas) ni para copys de marketing: esta skill produce mensajes, no piezas.
---

# Mensajes

Existe porque el problema casi nunca es escribir: es **decidir en qué tono**. Quien pregunta ya sabe
lo que quiere decir y se traba eligiendo el registro. Por eso el trabajo aquí es dar opciones
elegibles, no un mensaje único ni una clase de comunicación.

Regla que ordena todo lo demás: **el entregable es texto copiable**. Si hay que borrar algo antes de
pegarlo en WhatsApp, la respuesta falló.

## Flujo

1. **Leer el contexto.** Captura, texto pegado o la intención a secas. Identificar: quién es cada
   quien, qué se dijo último, qué medio es, qué relación hay (pareja potencial, cliente, jefe,
   proveedor), y cuánto tiempo pasó.
2. **Fijar el estilo.** Si el usuario lo nombró, ese. Si no, elegir el que corresponda y decirlo en
   una línea antes de las opciones — así puede corregir sin repetir todo el contexto.
3. **Generar 3-5 variantes** que se diferencien en *ángulo*, no en sinónimos. Tres formas de decir
   lo mismo no son opciones.
4. **Cerrar ofreciendo el ajuste**, en una línea: más corta, menos intensa, sin emoji, más formal.

## Estilos

### Social

| Estilo | Qué busca |
|---|---|
| `abrir` | Convertir un artefacto público — nota, estado, historia — en conversación privada |
| `gracioso` | Humor que salga del hilo, no chiste de catálogo |
| `coqueto` | Interés claro sin pedir permiso ni presionar |
| `provocativo` | Sube la tensión un escalón; se detiene antes de lo sexual explícito salvo que el hilo ya esté ahí |
| `interés genuino` | Pregunta que abre tema — una sola, no interrogatorio |
| `rescate` | La conversación murió: reactivarla sin reclamar la ausencia ni mendigar respuesta |
| `bajar un cambio` | Se pidió de más y frenaron: quitar la presión y reencuadrar sin retirarse del todo |
| `cerrar plan` | Pasar de charlar a proponer algo concreto: qué, cuándo, dónde. También cubre `salida` y `cita` |
| `incógnita` | Insinuar un plan sin revelarlo, para que la otra persona pregunte. Solo funciona si después hay plan de verdad |
| `cortar con elegancia` | Retirar el interés sin humillar ni dejar puerta falsa abierta |

> [!warning] "Salida" casi nunca significa `cortar con elegancia`
> En el español de Bolivia y buena parte de la región, "una salida" es **la cita**. Si alguien pide
> "algo de salida", casi siempre quiere `cerrar plan` o `incógnita`, no retirarse. Confirmarlo en
> media línea antes de generar, no después de tres opciones equivocadas.

### Trabajo y clientes

| Estilo | Qué busca |
|---|---|
| `firme y cordial` | Poner un límite sin romper la relación ni pedir disculpas por tenerlo |
| `cobro` | Pedir el pago pendiente con fecha y monto, sin tono de agencia de cobranza |
| `mala noticia` | Retraso, error propio, algo que no se puede hacer: decirlo primero, explicar después |
| `decir que no` | Rechazar alcance extra dejando abierta la vía pagada o la próxima |
| `desescalar` | El otro escribió enojado: bajar la temperatura sin darle la razón en lo que no la tiene |
| `seguimiento` | Tercer recordatorio que no suene a tercer recordatorio |

Los nombres no son decorativos: son el catálogo desde el que la persona elige sin tener que
formular un prompt. Si aparece una intención que ninguno cubre, nombrarla igual antes de responder
("esto es un *pedir disculpas sin arrastrarse*") — nombrar la intención es la mitad del trabajo.

## Formato de salida

Sin preámbulo. Sin repetir el contexto que la persona acaba de dar. Directo a las opciones.

```
Estilo: [nombre] · [medio]

**1.**
[mensaje, listo para copiar]
↳ [una línea: por qué funciona / cuándo elegir esta]

**2.**
[mensaje]
↳ [una línea]

**3.**
[mensaje]
↳ [una línea]

¿La ajusto? (más corta · menos intensa · sin emoji · más formal)
```

Cuando una opción carga riesgo — puede leerse pasivo-agresiva, demasiado directa, o le da a la otra
persona una salida fácil — decirlo en esa misma línea. Es más útil que entregarla limpia y que
explote después.

## Las siete reglas

1. **Español neutro.** Nada de voseo rioplatense ni modismos regionales, salvo que el hilo mismo los
   use — ahí sí, espejar.
2. **Longitud según el medio.** WhatsApp y DM: una o dos frases. Correo: dos o tres líneas más un
   cierre. Tres párrafos en un chat es un error de registro, no de contenido.
3. **Espejar el registro del otro.** Si escribe en minúsculas y sin tildes, no contestar como
   comunicado de prensa. Si es formal, no tutear de golpe.
4. **Sin emoji por defecto.** Solo si el hilo ya los usa, y como mucho uno.
5. **Prohibido inventar hechos.** Nada de precios, fechas, disponibilidad, nombres o promesas que no
   estén en el contexto. Donde falte un dato va un hueco visible: `[fecha]`, `[monto]`. Un mensaje
   con un dato inventado se envía y ya no se puede retirar — es el único error irreversible de esta
   skill.
6. **Marcar el riesgo** de la opción que pueda leerse mal. Una línea, sin sermón.
7. **Nunca suplantar identidad ni manipular.** Si lo que se pide es hacerse pasar por otra persona,
   fabricar una excusa falsa o presionar emocionalmente, decirlo en una frase y entregar la versión
   honesta que persigue el mismo objetivo. No moralizar más allá de eso.

## Timing

El mensaje correcto en el momento equivocado falla igual que el mensaje malo, así que decir *cuándo*
mandarlo es parte de la respuesta, no un extra.

Dos señales que cambian la recomendación, y que hay que buscar antes de opinar sobre el momento:

- **¿Sigue activa la otra persona?** Un "en línea" o "activo ahora", o el simple hecho de que acabe
  de contestar algo que podría haber dejado pasar, dice que la conversación está viva. Recomendar
  "espera a mañana" ahí desperdicia el pico. Solo conviene esperar si *ya se cerró* de verdad —
  despedida mutua y silencio.
- **¿Quién habló último?** Si fue la otra persona, hay entrada. Si fuiste vos y no hubo respuesta,
  el estilo real es `rescate`, no lo que se haya pedido.

La cortesía no es el criterio. La regla útil: mandar mientras la conversación esté en su punto más
alto y cerrar antes de que baje, en vez de estirarla hasta que se apague sola.

## Responder notas, estados e historias

Es un caso de entrada propio: no hay conversación, hay un artefacto público de una o dos palabras —
a veces solo emojis. Se responde distinto.

- **No interpretar en voz alta.** Analizar el significado de dos emojis mata el intercambio; la nota
  no es un acertijo, es una excusa para escribir.
- **Lo publicó para todos**, así que compite con las otras respuestas que va a recibir. La que gana
  es la que se puede contestar sin esfuerzo, no la más ingeniosa.
- **Ambigüedad a favor.** Si no se entiende la referencia, preguntar con humor funciona mejor que
  fingir que se entendió: da tema y le regala a ella el papel de explicar.
- **Corto.** Una línea. Una nota de dos emojis no se responde con tres frases.

## Leer una captura

La imagen trae más de lo que parece. Usar:

- **Quién está de qué lado**: las burbujas propias suelen ir a la derecha. Confirmarlo si es ambiguo
  en vez de asumir y responder por la persona equivocada.
- **Los tiempos**: "hace 3 días" cambia el mensaje por completo respecto de "hace 2 minutos". Si el
  hueco es largo, casi siempre el estilo real es `rescate` aunque hayan pedido otro.
- **El desequilibrio**: quién escribe párrafos y quién contesta con monosílabos. Eso decide cuánto
  invertir en el próximo mensaje.
- **La bio, el nombre de la empresa, lo que aparezca de fondo**: material gratis para personalizar.
- **Las señales de freno**, que son las que más se pasan por alto: `😅` o `🫣` junto a un "no sé",
  un "jaja" que responde a algo que no era chiste, o una respuesta más corta que las anteriores
  justo después de un pedido. Casi siempre significan que el último mensaje pidió de más — de
  intimidad, de datos o de compromiso. La respuesta correcta es `bajar un cambio`, no repetir el
  pedido con otras palabras. Cuando el hilo se traba, revisar primero **el último mensaje propio**:
  el problema suele estar ahí y no en el silencio del otro lado.

Si la captura no se entiende (recortada, ilegible, sin contexto suficiente), pedir **lo mínimo que
falta** y nada más. No devolver un cuestionario.

## Iteración

Cuando pidan un ajuste, entregar solo la versión corregida — no repetir las tres opciones enteras.
"Más corta" significa recortar, no reescribir con otro sentido.

Si dicen que ninguna sirve, el problema casi siempre es el estilo, no la redacción: proponer otro
estilo del catálogo antes de generar otra tanda igual.

## Ejemplos

**Petición:** *"Le escribí hace 4 días y me dejó en visto. Qué le pongo."*

```
Estilo: rescate · WhatsApp

**1.**
Oye, se me perdió esta conversación. ¿Cómo va tu semana?
↳ Asume el silencio como cosa de ambos. Sin reclamo, fácil de contestar.

**2.**
Vi algo hoy que me acordó de lo que hablaste del [tema]. Ahí te va.
↳ La mejor si tienes algo concreto que mandar: da motivo real, no solo saludo.

**3.**
¿Sigues por ahí o te secuestraron?
↳ Funciona si ya había humor entre ustedes. Si el hilo era formal, se lee raro.

¿La ajusto? (más corta · menos intensa · sin emoji · más formal)
```

**Petición:** *"El cliente me debe la segunda cuota desde hace tres semanas y ya le recordé dos veces."*

```
Estilo: cobro · correo

**1.**
Hola [nombre], te escribo por la segunda cuota de [monto], con vencimiento el [fecha].
¿Me confirmas la fecha en que queda pagada? Así ordeno la planificación de mi lado.
↳ Pide una fecha, no un pago. Mucho más difícil de dejar sin responder.

**2.**
Hola [nombre], quedó pendiente la segunda cuota de [monto]. Continúo con [entregable]
en cuanto esté regularizada.
↳ Vincula el pago al avance sin amenazar. Úsala si de verdad vas a detenerte.

**3.**
Hola [nombre], ¿hubo algún problema con la segunda cuota? Si necesitan otro plazo,
lo conversamos y lo dejamos por escrito.
↳ La más blanda. Abre la puerta a un plazo nuevo: elígela solo si estás dispuesto a darlo.

¿La ajusto? (más firme · más corta · con fecha límite explícita)
```

## Qué no hacer

- Entregar una sola opción. El valor está en elegir.
- Explicar teoría de la comunicación cuando lo que se pidió es un mensaje.
- Pedir contexto que ya está en la captura.
- Moralizar sobre para qué se usa.
- Rellenar con emoji, signos de exclamación o entusiasmo que la persona no traía.
