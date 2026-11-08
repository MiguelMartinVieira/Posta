# Posta // Design System & Brand Guidelines
> **Single Source of Truth (SSOT)** para la identidad visual, tokens de diseño, ingeniería frontend y directrices estéticas de **Posta**.  
> *Documento optimizado para ser consumido por agentes de IA, desarrolladores y diseñadores.*

---

## 1. Identidad de Marca y Posicionamiento

* **Nombre de la Empresa**: **Posta**
* **Tagline oficial**: *Red Predictiva de Pernocta y Tacógrafo*
* **Descriptor de producto**: *Plataforma B2B agnóstica de optimización de rutas, predicción de ocupación de áreas de descanso y cumplimiento legal de tacógrafo.*
* **Arquetipo estético**: **Infraestructura corporativa de alta gama (Estilo Suizo / Nórdico)**.
  * Inspiración: *Linear (modo claro), Stripe Dashboard, Apple Developer, Monotype Swiss Grid, Raycast*.
  * Atributos clave: **Sobriedad, máxima legibilidad, rigor legal, ligereza visual, ausencia de artificios y precisión subpíxel**.

---

## 2. Reglas Estrictas de Diseño ("Never" Rules)

Cualquier agente, diseñador o desarrollador que genere interfaces, diapositivas o creatividades para Posta debe cumplir estas reglas sin excepción:

1. **PROHIBIDO EL USO DE EMOJIS**: Bajo ningún concepto (nada de ⚡, 🟢, 🔴, ⚠️, 👁️, 🚛, etc.). En su lugar, usar **pastillas de estado tipográficas (*pills*)** con colores semánticos, nodos con micro-pulsos amortiguados o iconos vectoriales SVG limpios.
2. **PROHIBIDA LA ESTÉTICA DARK CYBERPUNK / GAMING**: No usar fondos negros con neones brillantes, ni destellos fluorescentes, ni degradados de ciencia ficción. La estética técnica nocturna de cabina se formula en Slate profundo (`oklch(12.88% 0.0406 264.7)` / `#020617`), nunca con negro puro saturado de colorines.
3. **SOMBRAS Y ELEVACIÓN MÍNIMAS ("ELEVACIÓN INVISIBLE")**: Las superficies se delimitan mediante **bordes técnicos de 1px** (`#E2E8F0` / `oklch(92.88% 0.0126 255.5)`) y **biseles de luz cenital interna** (`box-shadow: inset 0 1px 0 0 var(--inner-highlight)`). Prohibidas las sombras gaussianas difusas pesadas.
4. **DATOS NUMÉRICOS SIEMPRE MONOESPACIADOS Y TABULARES**: Tiempos de tacógrafo, matrículas, coordenadas, porcentajes y cifras económicas deben utilizar `JetBrains Mono` con alineación tabular (`font-variant-numeric: tabular-nums`) y cero barrado (`zero`).
5. **CERO COLISIÓN DE BORDES (NO BORDES DOBLES DE 2PX)**: Usar arquitectura de rejilla suiza con `gap: 1px` sobre fondo `--border-hairline`, o colapso negativo `margin: -1px` / `border-collapse: separate`.
6. **TRAZOS SVG INVARIANTES A LA ESCALA**: Todo elemento vectorial (`path`, `line`, `rect`, `polyline`) debe declarar `vector-effect="non-scaling-stroke"` para evitar distorsiones al redimensionar.

---

## 3. Logotipo e Isotipo Oficial

El isotipo representa un hito kilométrico y una ruta vial continua que asciende para formar la letra **P**, con un nodo interior que simboliza la plaza de pernocta asegurada en el camino.

### Código SVG Oficial (32x32)
```xml
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
  <rect width="32" height="32" rx="7" fill="#0F172A"/>
  <path d="M10 23V9H17.5C20.5376 9 23 11.2386 23 14C23 16.7614 20.5376 19 17.5 19H10" stroke="#FFFFFF" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" vector-effect="non-scaling-stroke"/>
  <circle cx="16.5" cy="14" r="2" fill="#0284C7"/>
</svg>
```

### Variante en Negativo / Solo Trazo (Para fondos oscuros o documentos impresos)
* Contenedor: `#0F172A` / `oklch(20.77% 0.0398 265.8)`.
* Trazo de la letra P: `#FFFFFF` (Blanco puro, 2.5px de grosor, remates redondeados).
* Punto de hito / nodo central: `#0284C7` (Azul cobalto institucional).

---

## 4. Tokens de Color (HEX y Espacio Perceptual OKLCH)

Posta utiliza una jerarquía cromática formulada en **OKLCH** para garantizar uniformidad perceptual entre matices, con equivalencias HEX para compatibilidad.

### 4.1. Escala Técnica Slate
| Token | HEX | OKLCH | Uso / Función |
| :--- | :--- | :--- | :--- |
| `--slate-50` / `--bg-page` | `#F8FAFC` | `oklch(98.42% 0.0034 247.9)` | Fondo general de aplicación diurna / reportes. |
| `--slate-100` / `--surface-subtle` | `#F1F5F9` | `oklch(96.83% 0.0069 247.9)` | Fondos de controles segmentados y cabeceras. |
| `--slate-200` / `--border-default` | `#E2E8F0` | `oklch(92.88% 0.0126 255.5)` | Borde canónico técnico de 1px. |
| `--slate-300` / `--border-strong` | `#CBD5E1` | `oklch(86.90% 0.0198 252.9)` | Bordes activos, foco y separadores destacados. |
| `--slate-400` / `--text-muted` | `#94A3B8` | `oklch(71.07% 0.0351 256.8)` | Metadatos, marcas de tiempo, etiquetas secundarias. |
| `--slate-500` / `--text-dim` | `#64748B` | `oklch(55.44% 0.0407 257.4)` | Iconos secundarios y rótulos de cabecera. |
| `--slate-700` | `#334155` | `oklch(37.17% 0.0392 257.3)` | Bordes sutiles en modo oscuro. |
| `--slate-800` | `#1E293B` | `oklch(27.95% 0.0368 260.0)` | Superficies elevadas en modo técnico cabina. |
| `--slate-900` / `--text-primary` | `#0F172A` | `oklch(20.77% 0.0398 265.8)` | Títulos principales, valores KPI, identificadores. |
| `--slate-950` / `--bg-canvas-dark` | `#020617` | `oklch(12.88% 0.0406 264.7)` | Fondo de cabina nocturna / canvas técnico. |

### 4.2. Color de Marca (Brand Core)
| Token | HEX | OKLCH | Uso / Función |
| :--- | :--- | :--- | :--- |
| `--brand-blue` | `#0284C7` | `oklch(58.30% 0.160 240.0)` | Color corporativo de acción, ruta activa de Posta, enlaces. |
| `--brand-blue-subtle` | `#E0F2FE` | `oklch(94.20% 0.038 238.0)` | Fondos de selección suave o badges corporativos. |

### 4.3. Semántica Operativa (Pernocta y Tacógrafo)
Generadas algorítmicamente mediante `color-mix(in oklch, var(--seed) X%, var(--surface))`:
* **Óptimo / Conforme / Libre**: `oklch(52.0% 0.145 155.0)` (Verde técnico sobrio).
* **Alerta / Preaviso 4h15m / Densidad >85%**: `oklch(64.0% 0.155 70.0)` (Ámbar instrumental).
* **Crítico / Infracción >4h30m / Completo**: `oklch(53.0% 0.185 25.0)` (Rojo ferroviario).
* **Descanso Reglamentario / Pausa**: `oklch(50.0% 0.130 255.0)` (Azul pizarra técnico).

### 4.4. Elevación Invisible y Bisel Cenital
```css
--inner-highlight: light-dark(oklch(100% 0 0 / 0.85), oklch(100% 0 0 / 0.05));
--panel-shadow: inset 0 1px 0 0 var(--inner-highlight), 0 1px 2px 0 oklch(20.77% 0.0398 265.8 / 0.03);
```

---

## 5. Tipografía de Alta Precisión e Ingeniería OpenType

* **Fuente de Interfaz (UI)**: `'InterVariable', 'Inter', -apple-system, BlinkMacSystemFont, sans-serif`
* **Fuente de Datos y Métricas**: `'JetBrains Mono Variable', 'JetBrains Mono', monospace`
* **Dimensionamiento Óptico**: `font-optical-sizing: auto;` activo en la raíz del documento.

### 5.1. Matriz de Registros OpenType
| Fuente | Registros Activos | Efecto Morfológico | Aplicación en Posta |
| :--- | :--- | :--- | :--- |
| **Inter** | `"cv02", "cv03", "cv04"` | Abre contraformas de dígitos 4, 6 y 9 | Lectura inmediata a micro-tamaños en tablas y mapas. |
| **Inter** | `"cv11"` | Conmuta 'a' a geométrica de un solo piso | Títulos, cabeceras de módulo y logomarca. |
| **Inter** | `"tnum", "zero"` | Números tabulares con cero barrado diagonal | Contadores, KPIs de cabecera y tablas comparativas. |
| **Inter** | `"calt", "case"` | Centra `:` entre cifras (10:30) y `-` en mayúsculas | Horarios, rangos (MAD -> FRA) e intervalos. |
| **JetBrains Mono** | `"zero"` | Sustituye el 0 punteado nativo por **cero barrado** | Homogeneización visual estricta con Inter. |
| **JetBrains Mono** | `"calt"` | Centrado vertical de `:` entre dígitos | Cronómetros de tacógrafo (04:15:00). |
| **JetBrains Mono** | `"ss01"` | Construcción técnica neutral (l simétrica, r abierta) | Telemetría G2V2, matrículas y tablas legales. |

> [!IMPORTANT]
> **Corrección de Bug en Chromium**: En Chrome, aplicar cualquier `letter-spacing` distinto de 0 desactiva por defecto `calt`. Se debe declarar obligatoriamente `"calt" 1, "liga" 1` en todo selector que aplique tracking negativo.

### 5.2. Escala de Tracking Semántico (Inter 4)
* **Display / Títulos XL (≥32px)**: `letter-spacing: -0.025em;` peso `600`, con `"cv11" 1, "calt" 1`.
* **KPIs y Cifras Destacadas (24px–30px)**: `letter-spacing: -0.020em;` peso `500-600`.
* **Subtítulos y Cabeceras de Módulo (15px–18px)**: `letter-spacing: -0.015em;` peso `600`.
* **Etiquetas y Filas (13px–14px)**: `letter-spacing: -0.010em;` peso `500`.
* **Texto Corrido de Lectura (13px–15px)**: `letter-spacing: 0em;` peso `400` (el tracking lo gestiona `opsz: auto`).
* **Pastillas y Cabeceras en Mayúsculas (10px–12px)**: `letter-spacing: 0.06em;` peso `600`, `text-transform: uppercase`.

---

## 6. Arquitectura de Superficies, Grillas y Trazos

### 6.1. Rejilla Bento Suiza de 1px (Cero Bordes Dobles)
Para evitar que dos tarjetas contiguas sumen sus bordes formando líneas de 2px:
```css
.posta-bento-grid {
  display: grid;
  gap: 1px;
  background-color: var(--border-default);
  border: 1px solid var(--border-default);
  border-radius: 4px;
  overflow: hidden;
}

.posta-bento-grid > * {
  background-color: var(--surface);
  box-shadow: inset 0 1px 0 0 var(--inner-highlight);
}
```

### 6.2. Fondos Técnicos con Máscara Radial Perimetral
La cuadrícula suiza ortogonal de 24px se genera en CSS puro y se desvanece con máscara para no colisionar con los bordes de las tarjetas:
```css
.posta-swiss-grid {
  position: relative;
  isolation: isolate;
}
.posta-swiss-grid::before {
  content: "";
  position: absolute;
  inset: 0;
  z-index: -1;
  pointer-events: none;
  background-image:
    linear-gradient(to right, color-mix(in oklch, var(--border-default) 65%, transparent) 1px, transparent 1px),
    linear-gradient(to bottom, color-mix(in oklch, var(--border-default) 65%, transparent) 1px, transparent 1px);
  background-size: 24px 24px;
  mask-image: radial-gradient(ellipse 85% 75% at 50% 35%, #000 35%, transparent 95%);
  -webkit-mask-image: radial-gradient(ellipse 85% 75% at 50% 35%, #000 35%, transparent 95%);
}
```

### 6.3. Trazos Vectoriales Invariantes (`vector-effect`)
Todos los elementos SVG técnicos deben declarar:
```css
svg path, svg line, svg polyline, svg rect {
  vector-effect: non-scaling-stroke;
}
```

---

## 7. Patrones de Componentes Nativos Modernos

### 7.1. Pastillas de Estado (Status Pills) con Pulso Amortiguado
Sin emojis. Tipografía monoespaciada con nodo semántico circular de 6px:
```html
<span class="posta-pill posta-pill--warning">
  <span class="posta-dot posta-dot--pulse" aria-hidden="true"></span>
  CONDUCCIÓN · 04:12 / 04:30
</span>
```
* **Comportamiento dinámico**: El pulso (`animation: posta-pulse 2.4s infinite`) se reserva exclusivamente para unidades con telemetría activa o alerta inminente. Los estados estacionarios usan nodo estático. Siempre respeta `@media (prefers-reduced-motion: no-preference)`.

### 7.2. Acordeón Técnico Nativo (`<details>` + `interpolate-size`)
Sin librerías JS para animar altura ni desplegables:
```html
<details class="posta-inspector" name="fleet-audit">
  <summary class="posta-inspector__summary">
    <span class="posta-license-plate">4890 MKL</span>
    <span class="posta-pill posta-pill--optimal">CONFORME</span>
  </summary>
  <div class="posta-inspector__body">
    <!-- Contenido con interpolate-size: allow-keywords -->
  </div>
</details>
```

### 7.3. Instrumentación Nativa con `<meter>`
Para tacógrafo y ocupación de SSTPA:
```html
<meter class="posta-meter" min="0" max="270" low="210" high="240" optimum="120" value="252">
  252 de 270 minutos
</meter>
```

### 7.4. Atajos de Teclado con `<kbd>` Mecánico de Bajo Perfil
```html
<kbd class="posta-kbd">⌘ R</kbd>
<kbd class="posta-kbd">ESC</kbd>
```

### 7.5. Control Segmentado (Segmented Buttons)
* Contenedor: Fondo `#F1F5F9`, borde `#E2E8F0`, `border-radius: 6px`, `padding: 2px`.
* Botón Inactivo: Fondo transparente, texto `#475569`, peso `500`.
* Botón Activo: Fondo `#FFFFFF`, texto `#0F172A`, peso `600`, `box-shadow: 0 1px 2px rgba(0,0,0,0.05), inset 0 1px 0 rgba(255,255,255,0.9)`.

---

## 8. Glosario Técnico Oficial (Lenguaje de la Marca)

Para redacciones de agentes, propuestas y demos, utilizar rigurosamente los términos aceptados por el sector:

* **SSTPA**: *Safe and Secure Truck Parking Areas* (Áreas de Aparcamiento Seguras y Protegidas para Camiones bajo estándar europeo Bronze/Silver/Gold/Platinum).
* **Tacógrafo Inteligente G2V2**: *Smart Tachograph Gen 2 Version 2* (Reglamento UE 2020/1054). Obligatorio en transporte internacional y extendido a furgonetas 2,5t–3,5t desde julio de 2026.
* **Control a 56 días**: El periodo legal de control retroactivo de la tarjeta de conductor en carretera.
* **FMS (Fleet Management System)**: Protocolo estándar de telemetría de pesados conectado al puerto CAN Bus.
* **Conducción Continua**: Tramo máximo de 4h 30m previo a la pausa obligatoria de 45 minutos (fraccionable únicamente en 15m + 30m en ese orden estricto, según Art. 7 Reg. 561/2006).
* **LOTT**: Ley de Ordenación de los Transportes Terrestres (marco sancionador español).
* **Artículo 12**: Disposición de excepción del Reg. 561/2006 para paradas imprevistas debidamente justificadas en el ticket del tacógrafo.

---

## 9. Drop-In Elevation Patch (Para Inyección Directa en HTML)

```css
/* ==========================================================================
   POSTA DESIGN SYSTEM — DROP-IN ELEVATION PATCH (SWISS PRECISION STANDARD)
   ========================================================================== */
:root {
  --font-sans: "InterVariable", "Inter", -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
  --font-mono: "JetBrains Mono Variable", "JetBrains Mono", ui-monospace, SFMono-Regular, monospace;
  --inner-highlight: rgba(255, 255, 255, 0.85);
}

@supports (interpolate-size: allow-keywords) {
  :root { interpolate-size: allow-keywords; }
}

html, body {
  font-family: var(--font-sans);
  font-optical-sizing: auto;
  font-feature-settings: "liga" 1, "calt" 1, "cv02" 1, "cv03" 1, "cv04" 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-rendering: optimizeLegibility;
}

h1, h2, h3, .brand-title, .panel-title, .kpi-value, .slide-title {
  font-feature-settings: "liga" 1, "calt" 1, "cv02" 1, "cv03" 1, "cv04" 1, "cv11" 1, "ss01" 1;
}

code, pre, .font-mono, .tacho-value, .license-plate, td[data-numeric="true"] {
  font-family: var(--font-mono);
  font-variant-numeric: tabular-nums slashed-zero;
  font-feature-settings: "calt" 1, "zero" 1, "ss01" 1;
}

svg path, svg line, svg polyline, svg rect {
  vector-effect: non-scaling-stroke;
}
```
