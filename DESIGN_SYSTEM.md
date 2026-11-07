# Posta // Design System & Brand Guidelines
> **Single Source of Truth (SSOT)** para la identidad visual, tokens de diseño, componentes y directrices estéticas de **Posta**.  
> *Documento optimizado para ser consumido por agentes de IA, desarrolladores y diseñadores.*

---

## 1. Identidad de Marca y Posicionamiento

* **Nombre de la Empresa**: **Posta**
* **Tagline oficial**: *Red Predictiva de Pernocta y Tacógrafo*
* **Descriptor de producto**: *Plataforma B2B agnóstica de optimización de rutas, predicción de ocupación de áreas de descanso y cumplimiento legal de tacógrafo.*
* **Arquetipo estético**: **Infraestructura corporativa de alta gama (Estilo Suizo / Nórdico)**.
  * Inspiración: *Linear (modo claro), Stripe Dashboard, Apple Developer, Monotype Swiss Grid*.
  * Atributos clave: **Sobriedad, máxima legibilidad, rigor legal, ligereza visual y ausencia de artificios**.

---

## 2. Reglas Estrictas de Diseño ("Never" Rules)

Cualquier agente o desarrollador que genere interfaces, diapositivas o creatividades para Posta debe cumplir estas reglas sin excepción:

1. **PROHIBIDO EL USO DE EMOJIS**: Bajo ningún concepto (nada de ⚡, 🟢, 🔴, ⚠️, 👁️, 🚛, etc.). En su lugar, usar **pastillas de estado tipográficas (*pills*)** con colores semánticos o iconos vectoriales SVG limpios.
2. **PROHIBIDA LA ESTÉTICA DARK CYBERPUNK / GAMING**: No usar fondos negros con neones brillantes, ni destellos fluorescentes, ni degradados de ciencia ficción.
3. **SOMBRAS Y ELEVACIÓN MÍNIMAS**: Las superficies se delimitan mediante **bordes técnicos de 1px (`#E2E8F0`)**, no con sombras difusas pesadas. Si se requiere elevación: `box-shadow: 0 1px 2px rgba(0,0,0,0.05)`.
4. **DATOS NUMÉRICOS SIEMPRE MONOESPACIADOS**: Tiempos de tacógrafo, matrículas, coordenadas, porcentajes y cifras económicas deben utilizar `JetBrains Mono` con alineación tabular (`font-variant-numeric: tabular-nums`).

---

## 3. Logotipo e Isotipo Oficial

El isotipo representa un hito kilométrico y una ruta vial continua que asciende para formar la letra **P**, con un nodo interior que simboliza la plaza de pernocta asegurada en el camino.

### Código SVG Oficial (32x32)
```xml
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
  <rect width="32" height="32" rx="7" fill="#0F172A"/>
  <path d="M10 23V9H17.5C20.5376 9 23 11.2386 23 14C23 16.7614 20.5376 19 17.5 19H10" stroke="#FFFFFF" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
  <circle cx="16.5" cy="14" r="2" fill="#0284C7"/>
</svg>
```

### Variante en Negativo / Solo Trazo (Para fondos oscuros o documentos impresos)
* Contenedor: `#0F172A` (Gris carbón profundo).
* Trazo de la letra P: `#FFFFFF` (Blanco puro, 2.5px de grosor, remates redondeados).
* Punto de hito / nodo central: `#0284C7` (Azul cobalto institucional).

---

## 4. Tokens de Color (Design Tokens)

### 4.1. Superficies y Neutros
| Token | HEX | Uso / Función |
| :--- | :--- | :--- |
| `--bg-page` | `#F8FAFC` | Fondo general de la aplicación y presentaciones. |
| `--surface` | `#FFFFFF` | Fondo de paneles, tarjetas, tablas y modales. |
| `--surface-subtle` | `#F1F5F9` | Fondos de controles segmentados, bloques de tacógrafo y cabeceras. |
| `--border-default` | `#E2E8F0` | Líneas de división, bordes de tarjeta (1px solido). |
| `--border-strong` | `#CBD5E1` | Bordes activos o de foco. |

### 4.2. Tipografía
| Token | HEX | Uso / Función |
| :--- | :--- | :--- |
| `--text-primary` | `#0F172A` | Títulos principales, valores KPI, identificadores. |
| `--text-secondary` | `#475569` | Textos explicativos, subtítulos, etiquetas activas. |
| `--text-muted` | `#94A3B8` | Metadatos, marcas de tiempo, etiquetas secundarias. |

### 4.3. Color de Marca (Brand Core)
| Token | HEX | Uso / Función |
| :--- | :--- | :--- |
| `--brand-blue` | `#0284C7` | Color corporativo de acción, ruta activa de Posta, enlaces. |
| `--brand-blue-subtle` | `#E0F2FE` | Fondos de selección suave o badges corporativos. |

### 4.4. Estados Semánticos (Status System)
*Nunca usar colores puros saturados. Usar siempre la tríada Fondo / Borde / Texto:*

```css
/* Estado Óptimo / Conforme / Garantizado */
--status-success-bg: #ECFDF5;
--status-success-border: #A7F3D0;
--status-success-text: #065F46;

/* Estado Alerta / Precaución / Densidad Alta */
--status-warning-bg: #FFFBEB;
--status-warning-border: #FDE68A;
--status-warning-text: #92400E;

/* Estado Infracción / Saturado / Colapso */
--status-danger-bg: #FEF2F2;
--status-danger-border: #FECACA;
--status-danger-text: #991B1B;
```

---

## 5. Tipografía y Jerarquía

* **Fuente de Interfaz (UI)**: `'Inter', -apple-system, BlinkMacSystemFont, sans-serif`
* **Fuente de Datos y Métricas**: `'JetBrains Mono', monospace`

### Escala Tipográfica
* **H1 / Título de Marca**: `18px`, peso `700`, `letter-spacing: -0.5px`.
* **H2 / Título de Módulo**: `15px`, peso `600`, `letter-spacing: -0.2px`.
* **Etiquetas de Panel / Sección**: `11px - 12px`, peso `600`, mayúsculas, `letter-spacing: 0.5px`, color `--text-secondary`.
* **Lectura General**: `13px`, peso `400`, interlineado `1.5`, color `--text-primary`.
* **Display de Tacógrafo**: `24px`, peso `700`, `JetBrains Mono`.

---

## 6. Patrones de Componentes Estándar

### 6.1. Pastillas de Estado (Pills en lugar de emojis)
```html
<!-- Conforme / Legal -->
<span class="pill pill-success font-mono">CONFORME</span>

<!-- Infracción Inminente -->
<span class="pill pill-danger font-mono">INFRACCIÓN PROYECTADA</span>
```
*Estilo*: `padding: 3px 8px; border-radius: 4px; font-size: 11px; font-weight: 600; text-transform: uppercase;`

### 6.2. Control Segmentado (Segmented Buttons)
* Contenedor: Fondo `#F1F5F9`, borde `#E2E8F0`, `border-radius: 6px`, `padding: 2px`.
* Botón Inactivo: Fondo transparente, texto `#475569`, peso `500`.
* Botón Activo: Fondo `#FFFFFF`, texto `#0F172A`, peso `600`, sombra `0 1px 2px rgba(0,0,0,0.05)`.

### 6.3. Directivas y Recomendaciones Algorítmicas
* Tarjeta con borde completo de 1px del color semántico.
* Título superior en negrita mayúscula (`11px - 12px`).
* Cuerpo explicativo conciso citando la acción y el beneficio (`13px`).
* Pie con separación tenue mostrando estado de la plaza y destino recomendado.

---

## 7. Glosario Técnico Oficial (Lenguaje de la Marca)

Para redacciones de agentes, propuestas y demos, utilizar rigurosamente los términos aceptados por el sector:

* **SSTPA**: *Safe and Secure Truck Parking Areas* (Áreas de Aparcamiento Seguras y Protegidas para Camiones).
* **Tacógrafo Inteligente G2V2**: *Smart Tachograph Gen 2 Version 2* (Reglamento UE 2020/1054).
* **Control a 56 días**: El nuevo periodo legal de control retroactivo en carretera.
* **FMS (Fleet Management System)**: Protocolo estándar de telemetría de pesados conectado al puerto CAN Bus.
* **Conducción Continua**: Tramo máximo de 4h 30m previo a la pausa obligatoria de 45 minutos.
* **LOTT**: Ley de Ordenación de los Transportes Terrestres (marco sancionador español).
* **Artículo 12**: Disposición de excepción del Reg. 561/2006 para paradas imprevistas.
