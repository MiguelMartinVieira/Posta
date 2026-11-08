# Posta // Design System & Brand Guidelines
> **Single Source of Truth (SSOT)** para la identidad visual, tokens de diseño, tipografía editorial y directrices estéticas de **Posta**.  
> *Documento optimizado para ser consumido por agentes de IA, desarrolladores y diseñadores.*

---

## 1. Identidad de Marca y Posicionamiento

* **Nombre de la Empresa**: **Posta**
* **Tagline oficial**: *La red de información y predicción al servicio de personas*
* **Descriptor de producto**: *Plataforma B2B agnóstica de optimización de rutas, predicción de ocupación de áreas de descanso (SSTPA) y cumplimiento legal de tacógrafo.*
* **Propósito nuclear**: **La tecnología al servicio de las personas**. No construimos software para vigilar al conductor, sino para devolver la certidumbre, la dignidad laboral y la seguridad física a quienes mueven la economía europea.
* **Arquetipo estético**: **Editorial Humanista de Alta Gama (Estilo Revista de Arquitectura & Fotografía Documental)**.
  * **Inspiración directa**: *Publicaciones de viajes y arquitectura de gran formato (estilo editorial 'Luxembourg'), fotografía cinematográfica de carretera, Swiss grid humanista, Monocle, Cereal, Kinfolk, Apple Human Stories*.
  * **Atributos clave**: **Tipografía suave con curvas orgánicas, minimalismo extremo en texto, gran escala visual, fotografía evocadora y alternancia radical de estados de ánimo (Dual-Mood System)**.

---

## 2. Reglas Estrictas de Diseño ("Never" Rules)

Cualquier agente, diseñador o desarrollador que genere interfaces, diapositivas o creatividades para Posta debe cumplir estas reglas sin excepción:

1. **MINIMALISMO TEXTUAL RADICAL ("MUY POCO TEXTO")**: Las presentaciones y creatividades de Posta cuentan historias humanas, no son manuales legales ni dashboards saturados. Los párrafos explicativos nunca superan las **2 o 3 líneas**. Si una idea puede transmitirse con un titular contundente, una cita textual y una métrica de choque, se elimina cualquier texto accesorio.
2. **TIPOGRAFÍA SUAVE CON CURVAS**: Los titulares principales no deben usar tipografías grotescas rígidas o cuadradas. Deben utilizar **`Syne`** (pesos 700 / 800), caracterizada por arcos curvos amplios y amables (en caracteres como 'S', 'O', 'C', 'R', 'G').
3. **SISTEMA DUAL-MOOD (PERSONAS VS. ALGORITMO)**:
   * **Modo Personas / Color**: Fondos limpios de papel editorial (`#FFFFFF` o `#F8F9FA`), acentos cálidos de luz de cabina y terracota (`#E26D46` / `#D97706`), y fotografía humana/escénica de gran formato.
   * **Modo Algoritmo / B&W**: Transición obligatoria a **Blanco y Negro puro** (`#090B0E` / `#FFFFFF`) para explicar la telemetría, el tacógrafo y el motor predictivo EAS. Cero color. La máquina se expresa en frialdad matemática monocroma para contrastar con la calidez humana.
4. **PROHIBIDO EL USO DE EMOJIS**: Sin excepción alguna (nada de ⚡, 🟢, 🔴, ⚠️, 👁️, 🚛, etc.). En su lugar, usar **pastillas tipográficas (*pills*)**, micro-bullets o iconos vectoriales SVG sobrios.
5. **PROHIBIDA LA ESTÉTICA GAMING / NEÓN CYBERPUNK**: Cero fondos negros con destellos morados o cian fluorescentes. El modo oscuro de Posta es de inspiración brutalista-editorial B&W, nunca gaming.
6. **DATOS NUMÉRICOS SIEMPRE MONOESPACIADOS Y TABULARES**: Horas (`21:18`), tiempos de tacógrafo (`04:30`), matrículas, porcentajes y cifras económicas se representan en `JetBrains Mono` con alineación tabular (`tabular-nums`).
7. **FOTOGRAFÍA DOCUMENTAL REAL**: Priorizar imágenes auténticas de carretera al atardecer, vistas de cabina, lluvia nocturna en el asfalto y áreas de descanso iluminadas. Prohibidos los renders 3D futuristas de camiones autónomos o el stock genérico de apretones de manos de oficina.
8. **ESTRUCTURA CANÓNICA DE PITCH DECK (13 DIAPOSITIVAS)**: Toda presentación ante inversores o jurados debe estructurarse obligatoriamente en los 4 bloques narrativos canónicos (*La Idea*, *La Solución*, *El Negocio*, *La Empresa*) y la contraportada animada con Miguel, Marius y el mosaico de 500.000 camioneros, detallada exhaustivamente en [PITCH_STRUCTURE.md](PITCH_STRUCTURE.md).

---

## 3. Logotipo e Isotipo Oficial

El isotipo representa un hito kilométrico y una ruta vial continua que asciende para formar la letra **P**, con un nodo interior que simboliza la plaza de pernocta asegurada en el camino.

### 3.1. Código SVG Oficial (32x32)
```xml
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
  <rect width="32" height="32" rx="7" fill="#0F172A"/>
  <path d="M10 23V9H17.5C20.5376 9 23 11.2386 23 14C23 16.7614 20.5376 19 17.5 19H10" stroke="#FFFFFF" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" vector-effect="non-scaling-stroke"/>
  <circle cx="16.5" cy="14" r="2" fill="#0284C7"/>
</svg>
```

### 3.2. Variantes de Aplicación Oficial
* **Variante Editorial / Humanista (Fondos Claros)**:
  * Contenedor: `#11141A` (Gris carbón editorial).
  * Trazo de la letra P: `#FFFFFF` (Blanco puro, 2.5px con remates redondeados).
  * Nodo central: `#E26D46` (Terracota cálido) o `#0284C7` (Azul institucional).
* **Variante Algoritmo B&W (Fondos Oscuros / Monocromo)**:
  * Contenedor: `#090B0E` con borde `rgba(255, 255, 255, 0.2)`.
  * Trazo de la letra P: `#FFFFFF`.
  * Nodo central: `#FFFFFF` o `#A1A1AA`.

---

## 4. Tokens de Color Oficiales (Dual-Mood Architecture)

Posta organiza su paleta en dos universos cromáticos estrictamente diferenciados:

```
┌────────────────────────────────────────────────────────┐
│             POSTA DUAL-MOOD ARCHITECTURE               │
├───────────────────────────┬────────────────────────────┤
│  1. MOOD PERSONAS (COLOR) │ 2. MOOD ALGORITMO (B&W)    │
│  - Papel Blanco Editorial │ - Negro Carbón Puro        │
│  - Terracota & Ámbar      │ - Blanco Titanio           │
│  - Fotografía Humana      │ - Gris Técnico Fiel        │
│  - Citas y Emoción        │ - Rigor y Precisión        │
└───────────────────────────┴────────────────────────────┘
```

### 4.1. Mood 1: El Factor Humano (Modo Papel Editorial / Color)
| Token | HEX | Función / Aplicación |
| :--- | :--- | :--- |
| `--paper-bg` | `#FFFFFF` | Fondo general de diapositivas y lienzos editoriales. |
| `--paper-surface` | `#F8F9FA` | Fondo de tarjetas de historia, paneles de cita y bloques de datos. |
| `--paper-border` | `#E5E7EB` | Líneas de división finas de 1px. |
| `--paper-text-main` | `#11141A` | Titulares principales, nombres propios y números de choque. |
| `--paper-text-muted` | `#64748B` | Subtítulos de lectura, pies de imagen y descripciones cortas. |
| `--paper-text-dim` | `#94A3B8` | Metadatos superiores, localizadores de ruta y marcas cronológicas. |
| `--accent-warm` | `#E26D46` | **Acento nuclear humano**: terracota editorial, citas directas y kickers. |
| `--accent-amber` | `#D97706` | Luz de cabina, estado de alerta empática y plazas aseguradas. |
| `--accent-blue` | `#0284C7` | Azul institucional Posta para identificadores corporativos y enlaces. |

### 4.2. Mood 2: El Algoritmo (Modo B&W / Precisión Matemática)
| Token | HEX | Función / Aplicación |
| :--- | :--- | :--- |
| `--bw-bg` | `#090B0E` | Fondo de diapositivas técnicas de algoritmia y computación telemática. |
| `--bw-surface` | `#12161E` | Superficies de contenedores de módulos de procesamiento (EAS / FMS). |
| `--bw-border` | `rgba(255, 255, 255, 0.14)` | Delimitaciones técnicas ultrafinas en 1px. |
| `--bw-text-main` | `#FFFFFF` | Títulos del motor predictivo, métricas de latencia y código. |
| `--bw-text-muted` | `#A1A1AA` | Descripciones de arquitectura técnica. |
| `--bw-text-dim` | `#71717A` | Rótulos de capas, identificadores de sensor y protocolos FMS. |

---

## 5. Tipografía Editorial y Curvas Suaves

```
       SYNE (DISPLAY)        →   Curvas generosas, amplias y elegantes
 PLUS JAKARTA SANS (BODY)    →   Legibilidad editorial y humanista
  JETBRAINS MONO (NUMBERS)   →   Telemetría de tacógrafo y datos tabulares
```

### 5.1. Jerarquía Tipográfica
* **Display / Título Hero (`Syne`, 700 / 800)**:
  * Tamaño: `64px – 96px`, `line-height: 0.95 – 1.05`, `letter-spacing: -2px a -2.5px`.
  * Uso: Palabra de marca (**POSTA**), titulares de apertura y cierre rotundos.
* **Titulares de Diapositiva (`Syne`, 700)**:
  * Tamaño: `36px – 48px`, `line-height: 1.1`, `letter-spacing: -1.2px`.
  * Mayúsculas estrictas para reforzar el carácter editorial de revista.
* **Kicker / Sobretítulo Superior (`Plus Jakarta Sans`, 700)**:
  * Tamaño: `11px – 12px`, mayúsculas, `letter-spacing: 2px – 3px`, color `--accent-warm`.
* **Citas Textuales de Conductores (`Plus Jakarta Sans`, Italic, 400)**:
  * Tamaño: `18px – 22px`, `line-height: 1.45`, acompañada de filete vertical de 2px en terracota.
* **Texto de Lectura / Leads (`Plus Jakarta Sans`, 400 / 500)**:
  * Tamaño: `15px – 16px`, `line-height: 1.5`, color `--paper-text-muted`. Máximo 3 líneas por bloque.
* **Métricas y Telemetría (`JetBrains Mono`, 700)**:
  * Tamaño: `48px – 64px` para cifras macro (`93%`, `75%`, `296K`), siempre con `tabular-nums`.

---

## 6. Patrones de Diseño Editorial (Component System)

### 6.1. Cabecera Fina de Metadatos (Top Meta-Bar)
Al estilo de las revistas internacionales de arquitectura y diseño, cada diapositiva abre con una línea superior minimalista:
```html
<div class="meta-bar">
  <div><span class="brand-bullet"></span>8 DE NOVIEMBRE DE 2026 · MADRID</div>
  <div>STARTCAMP 2026 · PITCH FINAL</div>
</div>
```
* **Estilo**: `font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 1.2px; color: var(--paper-text-muted);`
* **Bullet distintivo**: Círculo de 6px en terracota (`--accent-warm`) en diapositivas a color, o blanco puro en diapositivas B&W.

### 6.2. Marco Fotográfico Editorial (`.photo-frame`)
Las imágenes ocupan áreas amplias con esquinas sutilmente suavizadas (`border-radius: 6px`):
```html
<div class="photo-frame">
  <img src="path/to/highway.jpg" alt="Carretera al atardecer">
</div>
```
* Las fotografías deben tener alto contraste cromático o composiciones arquitectónicas limpias de calzadas, cabinas y áreas de servicio.

### 6.3. Bloque de Cita Humana Directa
```html
<div class="editorial-quote">
  «La gente ve una máquina de 40 toneladas estorbando. Yo solo pienso en ducharme con agua caliente y volver a casa con mis hijas.»
  <cite>— ANTONIO MORALES · CONDUCTOR PROFESIONAL</cite>
</div>
```

### 6.4. Columnas Técnicas en Mood B&W (El Algoritmo)
Para explicar la arquitectura técnica sin perder el aire sofisticado:
```html
<div class="grid-editorial-3">
  <div class="tech-column-bw">
    <span class="mono-label">01 // INGESTA CONTINUA</span>
    <h3 class="column-title">Telemetría FMS</h3>
    <p class="column-desc">Lectura agnóstica de tiempos en cientos de flotas en marcha.</p>
  </div>
  <!-- ... Columnas 02 y 03 -->
</div>
```

---

## 7. Glosario Técnico Oficial (Lenguaje de la Marca)

Para redacciones de agentes, propuestas y demos, utilizar rigurosamente los términos aceptados por el sector:

* **SSTPA**: *Safe and Secure Truck Parking Areas* (Áreas de Aparcamiento Seguras y Protegidas para Camiones bajo estándar europeo Bronze/Silver/Gold/Platinum).
* **Tacógrafo Inteligente G2V2**: *Smart Tachograph Gen 2 Version 2* (Reglamento UE 2020/1054). Obligatorio en transporte internacional y extendido a furgonetas 2,5t–3,5t desde julio de 2026.
* **Control a 56 días**: El periodo legal de control retroactivo de la tarjeta de conductor en carretera.
* **FMS (Fleet Management System)**: Protocolo estándar de telemetría de pesados conectado al puerto CAN Bus.
* **Conducción Continua**: Tramo máximo de 4h 30m previo a la pausa obligatoria de 45 minutos (fraccionable en 15m + 30m).
* **LOTT**: Ley de Ordenación de los Transportes Terrestres (marco sancionador español).
* **Artículo 12**: Disposición de excepción del Reg. 561/2006 para paradas imprevistas debidamente justificadas en el ticket del tacógrafo.

---

## 8. Drop-In Boilerplate CSS (Para Interfaces y Presentaciones)

```css
/* ==========================================================================
   POSTA EDITORIAL DESIGN SYSTEM — DROP-IN CSS BOILERPLATE
   ========================================================================== */
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,400;1,600&family=Syne:wght@600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap');

:root {
  /* Mood Color / Personas */
  --paper-bg: #FFFFFF;
  --paper-surface: #F8F9FA;
  --paper-border: #E5E7EB;
  --paper-text-main: #11141A;
  --paper-text-muted: #64748B;
  --accent-warm: #E26D46;
  --accent-amber: #D97706;
  --accent-blue: #0284C7;

  /* Mood B&W / Algoritmo */
  --bw-bg: #090B0E;
  --bw-surface: #12161E;
  --bw-border: rgba(255, 255, 255, 0.14);
  --bw-text-main: #FFFFFF;
  --bw-text-muted: #A1A1AA;

  /* Tipografías */
  --font-display: 'Syne', sans-serif;
  --font-body: 'Plus Jakarta Sans', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}

body {
  font-family: var(--font-body);
  background-color: var(--paper-bg);
  color: var(--paper-text-main);
  -webkit-font-smoothing: antialiased;
}

h1, h2, h3, .editorial-title {
  font-family: var(--font-display);
  letter-spacing: -0.025em;
  text-transform: uppercase;
}

.font-mono, [data-numeric="true"], .telemetry-val {
  font-family: var(--font-mono);
  font-variant-numeric: tabular-nums slashed-zero;
}
```
