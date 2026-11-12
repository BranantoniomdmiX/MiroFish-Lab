# VAMO — Paquete de experimento para MiroFish-Lab
**Experimento:** VAMO-001 — Simulación prospectiva de mercado, adopción y viabilidad comercial  
**Ámbito:** Moroleón y Uriangato, Guanajuato, México  
**Horizonte simulado:** 6 meses  
**Estado:** Material de entrada; no representa evidencia de mercado ni resultados reales.

## 1. Propósito y pregunta rectora

Explorar cómo podrían reaccionar clientes, comercios, motociclistas y competidores ante el lanzamiento de VAMO como plataforma/red local de entregas y mensajería en Moroleón y Uriangato. Identificar condiciones de adopción, barreras, riesgos operativos, sensibilidad al precio, economía unitaria y factores que harían viable o inviable el negocio.

**Pregunta rectora:** Bajo qué condiciones VAMO podría conseguir demanda recurrente, mantener una oferta suficiente de motociclistas y comercios, operar sin guerra de precios y alcanzar una economía sostenible durante sus primeros seis meses.

No producir una afirmación binaria o una predicción única sin intervalos, supuestos y escenarios alternativos.

## 2. Qué es VAMO y qué no es

VAMO se concibe como una red/plataforma de coordinación local de entregas, mensajería y mandados. En su operación inicial, una Central recibe y coordina los pedidos, asigna motociclistas y mantiene trazabilidad. WhatsApp es el canal inicial de entrada; la tecnología propia respalda folios, tarifas, asignaciones, estados, seguimiento, prueba de entrega y conciliación.

VAMO no debe confundirse con un restaurante, un marketplace de menús ni una flota propietaria de todas las motos. Los comercios mantienen sus negocios y los motociclistas participan en la red según las reglas comerciales del servicio. En el futuro se ha contemplado ofrecer la plataforma a otras flotas, pero esa expansión SaaS no forma parte del lanzamiento local inicial ni debe mezclarse con la estimación de demanda de este experimento.

## 3. Reglas operativas y económicas conocidas (datos de entrada, no hipótesis)

### 3.1 Tarifas locales de referencia actuales
| Zona | Distancia | Tarifa al cliente | Aporte Base en viajes calificantes |
|---|---:|---:|---:|
| Z1 | hasta 3.5 km | $35 MXN | $5 MXN |
| Z2 | 3.6–5.0 km | $45 MXN | $5 MXN |
| Z3 | 5.1–7.5 km | $55 MXN | $5 MXN |
| Z4 | 7.6–11 km | $85 MXN | $10 MXN |
| Z5 | 11.1–15 km | $115 MXN | $10 MXN |
| Z6 | 15.1–20 km | $150 MXN | $10 MXN |
| Fuera de cobertura | más de 20 km | sin tarifa automática | requiere validación |

Son las tarifas de referencia documentadas para el modelo actual. No asumir que ya fueron validadas comercialmente ni que reflejan la tarifa final de lanzamiento.

### 3.2 Economía del motociclista
- En el ciclo diario, los primeros 12 viajes calificantes pueden aportar a Base $5 (Z1–Z3) o $10 (Z4–Z6), con tope de $60 MXN.
- El último aporte se prorratea para nunca superar $60 acumulados.
- Al alcanzar el tope, los viajes siguientes del ciclo no tienen aporte a Base.
- El ciclo operativo de aportes corta a las 04:00.
- Los extras de Multi-Mandado y espera adicional pertenecen al motociclista conforme a las reglas vigentes.
- La simulación debe distinguir ingresos brutos del servicio, pago al motociclista, aporte a Base y extras. No sumar el precio íntegro del envío como ingreso de VAMO.

### 3.3 Multi-Mandado y espera
- Multi-Mandado: tarifa base más $15 por parada adicional en la misma ruta, o $20 si implica desvío a otra zona, según reglas.
- Hasta 20 minutos de espera incluidos.
- Desde el minuto 21: $1 MXN por minuto adicional, destinado al motociclista.

### 3.4 Comercios
Se han definido como propuestas comerciales:
- Emprendedor: $80–$100 MXN por semana.
- Socio VIP: $125–$150 MXN por semana.
Incluyen presencia en la red y beneficios de atención/publicidad según el plan. Estas cuotas son propuestas del modelo, no ventas ni aceptación verificadas. El costo del envío debe quedar separado de la cuota comercial. Los comercios no afiliados también pueden originar solicitudes de entrega: VAMO puede recoger en un negocio sin relación comercial formal con él.

### 3.5 Cliente
- Canal inicial de solicitud: WhatsApp.
- Cobertura local basada en distancia y zonas.
- Se ha contemplado lealtad 10+1, sujeto a reglas y presupuesto promocional. No asumir que está activo desde el día uno sin confirmación.
- El cliente debe poder conocer el estado y recibir información de seguimiento.

### 3.6 Operación y control
- No existe pedido sin folio; no se asigna motociclista sin folio; no se cierra servicio sin registrar resultado; ningún movimiento económico debe modificarse sin registro.
- La operación se coordina desde una Central, con atención humana para excepciones.
- La demanda puede llegar de clientes que quieren comprar/recoger en comercios afiliados y no afiliados.
- Se pretende reducir tiempo improductivo de los motociclistas y facilitar que encuentren destinos habituales.

## 4. Contexto geográfico y alcance

Mercado inicial de interés: Moroleón y Uriangato, Guanajuato. No asumir población exacta, penetración de internet, volumen de pedidos, cantidad de motos, número de comercios, ingresos promedio ni participación de mercado sin fuentes externas verificables. Si MiroFish necesita esos datos, marcarlos como desconocidos o crear rangos hipotéticos explícitos para sensibilidad; nunca presentarlos como hechos.

No extrapolar automáticamente a Yuriria, Cuitzeo, Acámbaro u otras ciudades.

## 5. Perfiles de agentes requeridos

Crear agentes heterogéneos y críticos, no promotores de VAMO. Cada agente debe tener objetivos, restricciones, nivel de sensibilidad al precio, confianza, hábitos, alternativas y posibilidad real de rechazar el servicio.

1. **Clientes potenciales (varios subtipos):**
   - comprador frecuente de comida;
   - persona que necesita farmacia/mandado urgente;
   - comprador ocasional de ropa, zapatos, refacciones o paquetes;
   - cliente sensible al precio;
   - cliente que prioriza rapidez y confianza;
   - cliente que prefiere recoger por sí mismo;
   - cliente que ya usa otro servicio o pide directamente al comercio.
2. **Comercios afiliables:**
   - pequeño comercio con poco personal;
   - restaurante con repartidor propio;
   - negocio con demanda irregular;
   - comercio con alto volumen y preocupación por tiempos;
   - dueño desconfiado de cuotas semanales.
3. **Comercios no afiliados:**
   - establecimiento que no conoce VAMO;
   - cadena o franquicia con procesos propios;
   - comercio que acepta que un tercero recoja el pedido, si sus reglas lo permiten;
   - comercio que rechaza intermediarios o exige pago previo.
4. **Motociclistas:**
   - trabajador que ya reparte para otros;
   - motociclista con disponibilidad parcial;
   - conductor que prioriza ingreso neto y poca espera;
   - conductor que compara tarifa/retención con competidores;
   - conductor que abandona si hay desorden, inseguridad o falta de viajes.
5. **Competidores y sustitutos:**
   - repartidor independiente que cobra $20–$25;
   - operador local que cobra alrededor de $30;
   - comercio con reparto propio;
   - cliente que solicita por WhatsApp directamente a un repartidor;
   - plataformas o alternativas disponibles, solo cuando haya evidencia o sean etiquetadas como hipotéticas.
6. **Central y socios operativos:**
   - operador que gestiona pedidos y excepciones;
   - responsable comercial que afilia negocios;
   - responsable financiero/control;
   - socios con disponibilidad limitada y prioridades distintas.

No inventar marcas ni atribuir conductas reales a empresas identificables si no hay fuentes.

## 6. Escenarios de simulación

Simular los escenarios por separado usando el mismo conjunto de reglas base. Mantener constantes las variables no modificadas en cada comparación.

### S1 — Conservador
Poca adopción inicial, baja confianza, escasos comercios afiliados, demanda dispersa, sensibilidad alta a precio y disponibilidad limitada de motociclistas.

### S2 — Base
Adopción gradual, algunos clientes recurrentes, mezcla de comercios afiliados y no afiliados, capacidad moderada y operación con recursos limitados.

### S3 — Favorable
Recomendación boca a boca, buena experiencia, repetición de pedidos, comercios que perciben valor y disponibilidad suficiente de motociclistas. No asumir éxito garantizado.

### S4 — Competencia de precio
Competidores que ofrecen $20, $25 o $30 MXN para recorridos locales comparables. Analizar qué clientes cambian, qué motociclistas cambian, impacto en calidad y si VAMO puede diferenciarse por confiabilidad, trazabilidad, cobertura y atención sin destruir margen.

### S5 — Estrés operativo
Picos simultáneos, pocos motociclistas conectados, negocios lentos, cancelaciones, direcciones incompletas, cambios de pedido, incidencias, fallas de internet y saturación de la Central.

### S6 — Baja afiliación comercial
Los clientes solicitan compras/recogidas en negocios no afiliados; medir oportunidades, fricción del proceso, rechazos del comercio, tiempos de espera y si el mapa de lugares recurrentes puede generar ventaja comercial posteriormente.

### S7 — Economía del motociclista
Comparar atractivo real del esquema de aportes durante los primeros 12 viajes/ciclo, tope $60, distancia, espera y frecuencia. Identificar qué nivel de viajes diarios hace atractivo o no el modelo para distintos perfiles.

## 7. Variables y sensibilidades

No tratar valores desconocidos como hechos. Probar rangos explícitos y explicar por qué se eligieron:
- Pedidos diarios: niveles bajo, medio y alto, definidos como supuestos de simulación.
- Pedidos por cliente por mes: bajo, medio y alto.
- Porcentaje de clientes que repite.
- Porcentaje de pedidos fuera de Z1.
- Tiempo de preparación/espera por comercio.
- Porcentaje de cancelación e incidencia.
- Motociclistas activos por turno y horas disponibles.
- Proporción de pedidos en comercios afiliados y no afiliados.
- Conversión de comercio prospecto a afiliado.
- Permanencia de comercios en planes semanales.
- Sensibilidad a tarifa $35 vs alternativas.
- Costos fijos reales y variables de la Central, canales, sistemas, publicidad, combustible si aplica al conductor, administración y promociones.

Para escenarios de tarifas, mantener como referencia las tarifas por zona actuales; solo variar tarifa cuando el escenario lo indique expresamente. No cambiar silenciosamente las reglas de aportación.

## 8. Preguntas que la simulación debe contestar

1. ¿Qué perfiles de cliente tienen mayor probabilidad simulada de probar VAMO y por qué?
2. ¿Qué perfiles repetirían y cuáles abandonarían?
3. ¿En qué circunstancias $35 hasta 3.5 km se percibe como justo, caro o barato?
4. ¿La diferenciación por confianza, cumplimiento, tracking y atención puede contrarrestar tarifas menores?
5. ¿Qué comercios pagarían una cuota semanal? ¿Qué beneficios valoran realmente?
6. ¿Qué barreras generan los comercios no afiliados?
7. ¿El esquema de aportes a Base atrae o desincentiva a los motociclistas?
8. ¿Qué volumen y distribución de pedidos hacen viable la disponibilidad de motos?
9. ¿En qué momentos la Central se satura?
10. ¿Qué errores pueden provocar pérdida de confianza?
11. ¿Qué condiciones permiten crecer sin comprar motos ni convertirse en una flota propietaria?
12. ¿Cuáles son las 10 causas más probables de fracaso?
13. ¿Qué cambios tienen mayor impacto positivo y cuáles solo agregan complejidad?
14. ¿Qué datos reales debe conseguir Jorge antes de invertir más dinero?
15. ¿Qué experimento barato podría refutar cada hipótesis clave?

## 9. Requisitos del informe

El informe final debe incluir:

- Resumen ejecutivo con nivel de confianza cualitativo y limitaciones.
- Descripción de agentes y supuestos.
- Tabla comparativa de escenarios S1–S7.
- Curvas o tablas mensuales de pedidos, usuarios recurrentes, comercios y conductores (si el motor permite estimaciones numéricas; marcar todo como simulado).
- Sensibilidad de precio.
- Economía unitaria separando tarifa cobrada, pago al motociclista, aporte a Base, extras, cuotas comerciales y costos operativos.
- Punto de equilibrio expresado en fórmula y escenarios, no inventar costos faltantes.
- Riesgos priorizados por impacto y facilidad de mitigación.
- Señales tempranas que indicarían que el negocio no funciona.
- Hipótesis más prometedoras.
- Experimentos reales de bajo costo para validar después.
- Decisión recomendada: CONTINUAR / AJUSTAR / PAUSAR / DESCARTAR, con argumentos y condiciones explícitas.

## 10. Reglas anti-alucinación y de honestidad

- No presentar la simulación como pronóstico estadístico, encuesta, estudio de mercado ni validación real.
- No inventar datos demográficos, competidores, cuotas de mercado, ingresos o volumen actual.
- Distinguir con etiquetas: DATO DEFINIDO, SUPUESTO, RESULTADO SIMULADO, DATO EXTERNO VERIFICADO, DATO DESCONOCIDO.
- Si los resultados dependen de un supuesto, mostrar cómo cambian al moverlo.
- No optimizar para que VAMO gane; el objetivo es descubrir si puede fracasar.
- No confundir facturación de envíos con ingreso de VAMO.
- No considerar la tarifa total del viaje como ingreso de Central.
- No afirmar que VAMO es rentable sin incluir costos.
- No usar una sola corrida como evidencia suficiente; realizar escenarios separados y, si es viable, varias semillas/corridas de bajo costo.

## 11. Configuración económica de la primera prueba

Comenzar con una prueba exploratoria pequeña: menos de 40 rondas por escenario, número moderado de agentes y solo los escenarios S1, S2, S4 y S5 en la primera tanda. No ejecutar todos los escenarios a máxima escala antes de revisar calidad y consumo. Guardar el costo aproximado de LLM por escenario y registrar configuración, modelo, rondas y fecha.

La segunda tanda (S3, S6, S7 y sensibilidad) se ejecutará únicamente tras revisar la primera salida.

## 12. Decisión que buscamos

La meta no es convencer a Jorge de seguir construyendo. La meta es proteger su tiempo y capital. MiroFish debe poder concluir que VAMO no es atractivo bajo determinados supuestos, o que conviene modificarlo o pausarlo.

**Principio:** Simular para cuestionar. Investigar para contrastar. Medir en el mercado antes de invertir más.
