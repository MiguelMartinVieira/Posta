# Datos del problema – POSTA (España)

## 1. Multas por pasarse de horas

| Exceso | Gravedad | Multa |
| --- | --- | --- |
| Hasta 1 hora | Leve | Unos 300–400 € |
| Más de 1 hora | Grave | 401–600 € |
| Más de 2 horas | Muy grave | 1.001–2.000 € y el camión inmovilizado |
| Más de un 25 % del límite semanal o quincenal | Muy grave | 4.001–6.000 € |

- La multa leve de 300–400 € sale de la prensa; no he podido confirmar el importe exacto en la ley.
- Las paga la empresa; si es autónomo, él mismo. Hay un 30 % de descuento si se pagan en los 30 días siguientes a la notificación.
- **Total en España:** unas 83.600 infracciones de tiempos al año (dato oficial) que suman **unos 59 M€ al año**. El importe es una estimación propia, con un rango de 30 a 84 M€.

## 2. Tiempo y gasóleo perdidos buscando sitio

Escenario realista: 45 minutos y 15 km extra al día, durante 230 días al año. Los minutos y los kilómetros son supuestos; los costes por hora y por kilómetro son oficiales.

| | Por camión y año | España (unos 39.000 camiones) |
| --- | --- | --- |
| Horas perdidas | 172 h | 6,7 M h |
| Gasóleo | 1.035 l (unos 1.970 €) | unos 77 M€ |
| **Coste total** | **10.123 €** | **unos 395 M€** |

Buscar sitio cuesta **unas 7 veces más que las multas**.

## 3. Precio: 15 € por camión al mes

| Argumento | Dato |
| --- | --- |
| Coste anual | 180 € por camión |
| Frente a lo que pierde un camión buscando sitio | Es el **1,8 %** de 10.123 € |
| Se paga con | **Unas 4 horas de conductor al año** |
| Una multa leve evitada | 300–400 €, casi **2 años de POSTA** |
| Comparables | Una noche de aparcamiento seguro cuesta 15–35 €; una plataforma de flota, 15–35 €/vehículo/mes |

**Qué incluye:**

- Ocupación medida y predicción de las áreas de España.
- Paradas planificadas según el tacógrafo de cada camión.
- Alertas cuando el área prevista se va a llenar.
- Reservas en aparcamientos seguros.
- Un informe para justificar un exceso. No está garantizado que sirva: lo decide el agente o el juez.

**Riesgo:** LKW.APP ya ofrece predicción gratis al conductor. Hay que validar el precio con las primeras flotas.

## 4. TAM, SAM y SOM (a 15 €/camión/mes)

El mercado son los clientes que pagarían por información predictiva de ocupación de áreas de servicio para camiones. No es lo que se paga en multas ni lo que se pierde buscando sitio, sino lo que esos clientes gastarían en una solución como POSTA.

**Precios usados.** Son supuestos propios basados en comparables; no hay precios públicos de una API de ocupación de aparcamientos.

| Cliente | Qué paga | Precio |
| --- | --- | --- |
| Empresa de transporte | Plan Pro por camión | 15 €/camión/mes (180 €/año) |
| Operador de área de servicio | Cámaras, panel y publicación en el Punto de Acceso Nacional (NAP) | 1.200 €/área/año (supuesto) |
| Plataforma de navegación, de flotas o logística | Licencia de datos o API | 100.000 €/año (supuesto; rango 50.000–150.000) |

### TAM – Mercado total (Unión Europea)

Todas las empresas que podrían necesitar POSTA, sin límite geográfico ni comercial. Se toma la UE porque fuera de ella (EE. UU., por ejemplo) cambian la normativa, el tacógrafo y los competidores, y no hay datos comparables.

| Cliente | Cálculo | Valor al año |
| --- | --- | --- |
| Empresas de transporte | 6,2 M camiones medios y pesados × 180 € | 1.116 M€ |
| Operadores de áreas de servicio | 6.500 áreas × 1.200 € | 7,8 M€ |
| Plataformas de navegación, flotas y logísticas | unas 100 plataformas (supuesto) × 100.000 € | 10 M€ |
| **TAM** | | **unos 1.134 M€** |

### SAM – Mercado accesible (España, Francia y Portugal)

La parte del TAM a la que POSTA puede llegar con su producto en estos tres países. Solo cuentan los camiones de larga distancia, que son los que duermen fuera y buscan área.

| Cliente | Cálculo | Valor al año |
| --- | --- | --- |
| Empresas de transporte | 1,32 M camiones medios y pesados (Francia 616.467, España 571.927, Portugal 135.000) × 40 % de larga distancia (supuesto) = 529.000 camiones × 180 € | 95,3 M€ |
| Operadores de áreas de servicio | unas 1.340 áreas (supuesto: la misma proporción que los camiones, el 20,6 % de la UE) × 1.200 € | 1,6 M€ |
| Plataformas que operan en los tres países | unas 40 (supuesto) × 100.000 € | 4 M€ |
| **SAM** | | **unos 101 M€** |

### SOM – Mercado capturable (España, unos 3 años)

Lo que POSTA puede conseguir de verdad, teniendo en cuenta a la competencia (LKW.APP, Bosch, TRAVIS, SNAP, Mowiz) y a un equipo pequeño.

| Cliente | Supuesto | Valor al año |
| --- | --- | --- |
| 15 empresas de transporte en directo | 50 camiones de media = 750 camiones × 180 € | 135.000 € |
| 3 plataformas de flota o logísticas integradas | Licencia de 100.000 € cada una | 300.000 € |
| Camiones que llegan a través de esas 3 plataformas | 2.000 camiones por plataforma = 6.000 × 180 € | 1.080.000 € |
| 10 operadores de áreas de servicio | 5 áreas cada uno = 50 áreas × 1.200 € | 60.000 € |
| **SOM** | | **unos 1,58 M€** (alrededor del 1,6 % del SAM) |

**Lectura.**

- **Los camiones que llegan por plataformas** son casi el 70 % del SOM, así que la prioridad son las integraciones y no vender flota a flota.
- **Para llegar a unos 3 M€** harían falta unos 14.000 camiones a través de plataformas, en vez de 6.000.
- **Este cálculo da por hecho que se consiguen los mismos clientes que a 5 €.** Con el triple de precio, lo normal es que entren menos. Además, si la plataforma se queda, por ejemplo, el 30 % del precio, el SOM baja. Hay que validarlo con las primeras flotas.

## 5. Ejemplo: un autónomo

- **Cada control revisa 28 días.** El agente mira el día en curso y los 28 anteriores, y cada exceso se multa por separado.
- **Te paran más o menos una vez al año.** En España se controlan unos 233.000 conductores al año en carretera, del orden de un control por camión.
- **El caso de Juan** (sus hábitos son un supuesto): dos veces por semana se pasa unos 15 minutos buscando sitio.
  - En los 28 días que revisa un control acumula unos 8 excesos leves.
  - Eso suma **2.400–3.200 € de golpe**, o 1.680–2.240 € si paga pronto.
  - Además, pierde unos **10.100 € al año** buscando sitio.
  - POSTA le costaría **180 € al año**.

## Fuentes

- [Comisión Europea, SWD(2024) 215](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX%3A52024SC0215): infracciones y controles
- [Comisión Europea: estudio sobre aparcamiento seguro (2025)](https://transport.ec.europa.eu/news-events/news/more-safe-and-secure-parking-professional-drivers-needed-eu-study-reveals-2025-04-11_en)
- [Observatorio de costes del Ministerio de Transportes](https://cdn.transportes.gob.es/portal-web-transportes/transporte-terrestre/actividades-servicios/observatorios-costes-transporte-mercancias/2026/Observatorio%20Costes%20Mercanc%C3%ADas_2026-01%20Enero.pdf)
- [LOTT, Ley 16/1987](https://www.boe.es/buscar/act.php?id=BOE-A-1987-16760)
- [ACEA, Vehicles in use 2023](https://www1.pzpm.org.pl/pl/content/download/15673/108016/file/ACEA-report-vehicles-in-use-europe-2023.pdf)
- [Precios de Webfleet (subger.com)](https://subger.com/en/service/webfleet-solutions)
