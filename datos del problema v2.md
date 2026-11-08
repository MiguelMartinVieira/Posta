# Datos del problema – POSTA (España)

## 1. Cuánto cuestan las multas por pasarse de horas

| Exceso sobre la conducción diaria (9 h, o 10 h dos días por semana) | Gravedad | Multa |
| --- | --- | --- |
| Hasta 1 hora (10, 15, 59 minutos) | Leve | Unos 300–400 € |
| Más de 1 hora | Grave | 401–600 € |
| Más de 2 horas | Muy grave | 1.001–2.000 € y el camión inmovilizado |
| Más de un 25 % sobre el límite semanal (56 h) o de dos semanas (90 h) | Muy grave | 4.001–6.000 € |
| Reincidencia en muy grave en 12 meses | Muy grave | Hasta 18.000 € |

- La multa leve de 300–400 € sale de la prensa; no he podido confirmar el importe exacto en la ley.
- Si se paga en los 30 días siguientes a la notificación, hay un 30 % de descuento.
- Paga la empresa titular del camión (LOTT). Si es autónomo, paga él.

## 2. Cuánto pagan las empresas en total al año

- **Dato oficial:** unas 83.600 infracciones de tiempos al año en España (conducción, pausas y descansos; media de 2021–2022, Comisión Europea). Son infracciones, no conductores: un mismo conductor puede acumular varias.
- **Dato que no existe:** nadie publica cuánto se recauda. Por eso lo estimo multiplicando por una multa media:

| Escenario | Multa media | Total al año |
| --- | --- | --- |
| Bajo (media real de Aragón en 2024) | 363 € | **unos 30 M€** |
| Medio | 700 € | **unos 59 M€** |
| Alto | 1.000 € | **unos 84 M€** |

## 3. Dinero perdido en tiempo y gasóleo buscando otra área de servicio

**Cómo se calcula.** Por camión y año:

> (minutos perdidos al día / 60 × 44,47 €/h + km extra al día × 0,71 €/km) × 230 días

- **Coste por hora de un articulado de 44 t:** 44,47 €/h (dato oficial del Observatorio de costes del Ministerio de Transportes, octubre de 2025).
- **Coste por kilómetro:** 0,71 €/km, que ya incluye gasóleo, neumáticos y mantenimiento (mismo Observatorio).
- **Gasóleo:** 1,90 €/l (media nacional, 1 de noviembre de 2026).
- **Supuestos propios:** el consumo (30 l/100 km) y los 230 días al año con parada nocturna fuera de casa.
- **Camiones afectados:** unos 39.000 camiones duermen fuera cada noche en España. Es una estimación a partir de la demanda ibérica del estudio de la Comisión Europea (2025).
- **Minutos y kilómetros de búsqueda:** son supuestos. La Comisión cita unos 45 minutos diarios, pero no hay ninguna medición española.

**Por camión y año**

| Escenario | Búsqueda al día | Horas perdidas al año | Km extra al año | Gasóleo al año | Coste del tiempo | Coste de los km | **Total por camión** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Conservador | 20 min y 5 km | 77 h | 1.150 km | 345 l (unos 660 €) | 3.409 € | 817 € | **4.227 €** |
| Realista | 45 min y 15 km | 172 h | 3.450 km | 1.035 l (unos 1.970 €) | 7.671 € | 2.452 € | **10.123 €** |
| Pesimista | 60 min y 25 km | 230 h | 5.750 km | 1.725 l (unos 3.280 €) | 10.228 € | 4.087 € | **14.315 €** |

El gasto en gasóleo ya está dentro del coste de los km; aparece aparte para que se vea.

**Total en España al año (unos 39.000 camiones)**

| Escenario | Horas perdidas | Gasóleo | Coste del tiempo | Coste de los km | **Total** |
| --- | --- | --- | --- | --- | --- |
| Conservador | 3,0 M h | 13,5 M l (unos 26 M€) | 133 M€ | 32 M€ | **unos 165 M€** |
| Realista | 6,7 M h | 40,4 M l (unos 77 M€) | 299 M€ | 96 M€ | **unos 395 M€** |
| Pesimista | 9,0 M h | 67,3 M l (unos 128 M€) | 399 M€ | 160 M€ | **unos 559 M€** |

**Conclusión:** en el escenario realista, buscar sitio cuesta unos 395 M€ al año. Es unas 7 veces más que todas las multas de tiempos juntas (unos 59 M€). El dinero está en el tiempo y el gasóleo, no en las multas.

## 4. TAM, SAM y SOM de POSTA

El mercado son los clientes que pagarían por información predictiva de ocupación de áreas de servicio para camiones. No es lo que se paga en multas ni lo que se pierde buscando sitio, sino lo que esos clientes gastarían en una solución como POSTA.

**Precios de referencia.** Son supuestos propios basados en comparables; no hay precios públicos de una API de ocupación de aparcamientos.

| Cliente | Qué paga | Precio supuesto | Comparable |
| --- | --- | --- | --- |
| Empresa de transporte | Módulo por camión | 5 €/camión/mes (60 €/año) | Las plataformas de flota completas cuestan 15–35 €/vehículo/mes |
| Operador de área de servicio | Cámaras, panel y publicación en el Punto de Acceso Nacional (NAP) | 1.200 €/área/año | Sin referencia pública |
| Plataforma de navegación, de flotas o logística | Licencia de datos o API | 100.000 €/año (rango 50.000–150.000) | Sin referencia pública |

### TAM – Mercado total (Unión Europea)

Todas las empresas que podrían necesitar POSTA, sin límite geográfico ni comercial. Se toma la UE porque fuera de ella (EE. UU., por ejemplo) cambian la normativa, el tacógrafo y los competidores, y no hay datos comparables.

| Cliente | Cálculo | Valor al año |
| --- | --- | --- |
| Empresas de transporte | 6,2 M camiones medios y pesados × 60 € | 372 M€ |
| Operadores de áreas de servicio | 6.500 áreas × 1.200 € | 7,8 M€ |
| Plataformas de navegación, flotas y logísticas | unas 100 plataformas (supuesto) × 100.000 € | 10 M€ |
| **TAM** | | **unos 390 M€** |

### SAM – Mercado accesible (España, Francia y Portugal)

La parte del TAM a la que POSTA puede llegar con su producto en estos tres países. Solo cuentan los camiones de larga distancia, que son los que duermen fuera y buscan área.

| Cliente | Cálculo | Valor al año |
| --- | --- | --- |
| Empresas de transporte | 1,32 M camiones medios y pesados (Francia 616.467, España 571.927, Portugal 135.000) × 40 % de larga distancia (supuesto) = 529.000 camiones × 60 € | 31,8 M€ |
| Operadores de áreas de servicio | unas 1.340 áreas (supuesto: la misma proporción que los camiones, el 20,6 % de la UE) × 1.200 € | 1,6 M€ |
| Plataformas que operan en los tres países | unas 40 (supuesto) × 100.000 € | 4 M€ |
| **SAM** | | **unos 37 M€** |

### SOM – Mercado capturable (España, unos 3 años)

Lo que POSTA puede conseguir de verdad, teniendo en cuenta a la competencia (Bosch, TRAVIS, SNAP, HERE, Mowiz) y a un equipo pequeño.

| Cliente | Supuesto | Valor al año |
| --- | --- | --- |
| 15 empresas de transporte en directo | 50 camiones de media = 750 camiones × 60 € | 45.000 € |
| 3 plataformas de flota o logísticas integradas | Licencia de 100.000 € cada una | 300.000 € |
| Camiones que llegan a través de esas 3 plataformas | 2.000 camiones por plataforma = 6.000 × 60 € | 360.000 € |
| 10 operadores de áreas de servicio | 5 áreas cada uno = 50 áreas × 1.200 € | 60.000 € |
| **SOM** | | **unos 0,77 M€** (alrededor del 2 % del SAM) |

**Lectura.** Con estos precios, el SOM ronda los 0,8 M€, no los 3 M€ del ejemplo. Casi el 90 % llega por las plataformas, así que la prioridad comercial son las integraciones y no la venta flota a flota. Para llegar a unos 3 M€ haría falta, por ejemplo, unos 30.000 camiones a través de plataformas o licencias de datos más caras. Los dos son supuestos que hay que validar en las primeras conversaciones con plataformas.

**Comparado con el problema.** Las multas de tiempos en España suman unos 59 M€ al año (apartado 2) y el tiempo y el gasóleo perdidos, unos 395 M€ (apartado 3). Ese es el valor que POSTA ayuda a ahorrar a sus clientes. El mercado de POSTA (lo que esos clientes le pagarían) es mucho menor.

## 5. Cada cuánto llegan las multas: el caso de un autónomo

**Cómo funciona un control.** En un control en carretera el agente revisa **el día en curso y los 28 días anteriores** del tacógrafo. Cada exceso de esos días se puede multar por separado, así que un solo control puede traer varias multas a la vez. En una inspección en la empresa pueden revisar hasta un año de registros.

**Cada cuánto te paran.** En España se controlan unos 233.000 conductores al año en carretera. Eso sale, de forma muy aproximada, a **un control por camión y año**.

**Ejemplo (los hábitos de Juan son un supuesto):** Juan es autónomo con un camión y hace la AP-7. Dos veces por semana encuentra el área llena y se pasa unos 15 minutos del límite buscando otra.

- En los 28 días que revisa el control acumula unos **8 excesos leves**.
- 8 × 300–400 € = **2.400–3.200 €**, o **1.680–2.240 €** si paga pronto.
- Le llega todo de golpe, una vez al año, por excesos que le costaron 15 minutos cada uno.
- Si alguno de esos días se pasa más de 2 horas, esa multa sola ya es de 1.001–2.000 € y le inmovilizan el camión.
- En Portugal, cada exceso de 5 a 15 minutos puede costar más de 2.000 €.
- Además, en el escenario realista Juan pierde unos 10.100 € al año buscando sitio (apartado 3), entre 3 y 4 veces lo que paga en multas.

## Fuentes

- Comisión Europea (2024). [Informe de aplicación de la normativa social, SWD(2024) 215](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX%3A52024SC0215): infracciones y controles 2021–2022.
- Comisión Europea (2025). [Estudio sobre aparcamiento seguro para conductores profesionales](https://transport.ec.europa.eu/news-events/news/more-safe-and-secure-parking-professional-drivers-needed-eu-study-reveals-2025-04-11_en): demanda de aparcamiento y los 45 minutos de búsqueda.
- Ministerio de Transportes. [Observatorio de costes del transporte de mercancías por carretera](https://cdn.transportes.gob.es/portal-web-transportes/transporte-terrestre/actividades-servicios/observatorios-costes-transporte-mercancias/2026/Observatorio%20Costes%20Mercanc%C3%ADas_2026-01%20Enero.pdf): costes por hora y por kilómetro.
- [LOTT, Ley 16/1987](https://www.boe.es/buscar/act.php?id=BOE-A-1987-16760), artículos 140 a 143: cuantías de las multas.
- ACEA. [Vehicles in use – Europe 2023](https://www1.pzpm.org.pl/pl/content/download/15673/108016/file/ACEA-report-vehicles-in-use-europe-2023.pdf): camiones medios y pesados por país (datos de 2021). [ACEA 2026](https://www.fxbaogao.com/detail/5228193): 6,2 M en la UE (datos de 2024).
- Gobierno de Aragón (2024). [Indicadores del plan de inspección](https://transparencia.aragon.es/sites/default/files/documents/indicadores_ejecucion_plan_inspeccion_aragon_2024.pdf): multa media de 363 €.
