# Tema 11 — Changelog (v1.0 → v2.0 → v3.0)

> **Versiones**:
> - v1.0 (2026-04-16) — primera versión del piloto.
> - v2.0 (2026-04-23) — iteración tras feedback de María (21 abr 2026).
> - **v3.0 (2026-04-28) — iteración tras revisión de María/Ana: ampliación de tipos de datos, elementos de SI y características de SI.**

---

## Cambios v3.0 — Resumen

| Aspecto | v2.0 | v3.0 | Δ |
|---|---|---|---|
| Palabras | ~14.300 | ~19.500 | +36% |
| Subsecciones nuevas en 1.7 | 4 (función, naturaleza, variabilidad, estructura) | 9 (añadidas: primitivos, compuestos, TAD, SQL, tipado) | +5 |
| Detalle componentes SI (§2.2) | Tabla 7 filas + 1 frase | 7 componentes con subcomponentes y normas | +1.500 palabras |
| Detalle características SI (§2.3) | Lista 10 viñetas | 10 características con métricas, normas y ejemplo Ayto | +1.500 palabras |
| Fuentes Tier 1 añadidas | 18 | 28 | +10 |

### Cambios v3.0 por sección

**Sección 1.7 — Tipos y clasificación de datos**:
- Renombrada de "Clasificación de datos" a "Tipos y clasificación de datos".
- Añadida referencia a ISO/IEC 11404 (norma de tipos independientes de lenguaje).
- Nueva subsección **1.7.5 Tipos primitivos**: tabla con familias (enteros, reales, lógicos, carácter), tamaños en bytes, rangos completos, ejemplos en Java/C/Python.
- Nueva subsección **1.7.6 Tipos compuestos**: array, struct, union, enum, string.
- Nueva subsección **1.7.7 Tipos abstractos de datos (TAD)**: tabla con 8 TAD canónicos (pila, cola, lista, conjunto, mapa, árbol, grafo, cola de prioridad) con operaciones, política de acceso y casos de uso.
- Nueva subsección **1.7.8 Tipos SQL**: catálogo completo según ISO/IEC 9075 (SQL:2016).
- Nueva subsección **1.7.9 Tipado en lenguajes**: ejes estático/dinámico y fuerte/débil con tabla comparativa Java/Python/JavaScript/C/TypeScript.
- Nuevo callout DATO CLAVE: ejes tipado independientes.
- Nuevo callout DATO CLAVE: IEEE-754 con desglose float/double.

**Sección 2.2 — Componentes básicos del SI**:
- Añadido bloque "Detalle de cada componente" con subcomponentes para los 7 componentes:
  - Hardware: equipos centrales, cliente, almacenamiento, E/S, red.
  - Software: 4 capas (sistema, utilidad, middleware, aplicación) según ISO/IEC 25010.
  - Datos: OLTP, DWH/OLAP, Data Lake, ficheros, metadatos.
  - Procedimientos: manuales, políticas seguridad, procesos BPMN, SLA, BCP/DRP.
  - Usuarios: 5 roles (administradores, funcionales, externos, auditores, dirección).
  - Red: por alcance (PAN/LAN/CAN/MAN/WAN), por uso (intranet/extranet/Internet), por topología, servicios.
  - Retroalimentación: KPI, encuestas, ITSM, auditorías, ciclo PDCA.
- Nuevo callout DATO CLAVE: tres bloques TI/organización/personas (visión tripartita COBIT 2019, ITIL v4 cuatro dimensiones).

**Sección 2.3 — Características del SI**:
- Tabla resumen al inicio: característica, cómo se mide, norma de referencia.
- Detalle individual de las 10 características, cada una con:
  - Definición ampliada.
  - Cómo se mide (uptime, MTBF, MTTR, P50/P95/P99, RTO/RPO, etc.).
  - Norma técnica de referencia (ISO/IEC 25010, ISO 8000, ISO 27001, ISO/IEC 27040, ENS, RD 1112/2018, UNE-EN 301 549, WCAG 2.1).
  - Ejemplo aplicado al Ayto Madrid (Sede Electrónica, datos.madrid.es, Padrón, IBI, cita previa, etc.).
- Nuevo callout DATO CLAVE: tríada CIA + trazabilidad + autenticidad (ENS).
- Nuevo callout DATO CLAVE: ISO/IEC 25010 SQuaRE — 8 características de calidad de software.

### Fuentes añadidas en v3.0

| Fuente | Motivo |
|---|---|
| ISO-25010 | Modelo de calidad de software para características SI (§2.3) |
| ISO-11404 | Tipos de datos primitivos independientes de lenguaje (§1.7.5) |
| ISO-9075 | Catálogo de tipos SQL:2016 (§1.7.8) |
| KNUTH-TAOCP | Tipos abstractos de datos (§1.7.7) |
| DAMA-DMBOK | Marco de gestión de datos (§2.3) |
| RD-1112-2018 | Accesibilidad sitios web sector público español (§2.3) |
| UNE-301549 | Norma europea de accesibilidad TIC (§2.3) |
| ITIL-4 | Cuatro dimensiones de gestión de servicios (§2.2) |
| COBIT-2019 | Visión tripartita TI-organización-personas (§2.2) |

---

## Cambios v2.0 — Resumen (histórico)

> **Fecha**: 2026-04-23
> **Autor**: MGS
> **Motivo**: Iteración tras feedback de María (21 abr 2026)

---

## Resumen de cambios

| Aspecto | v1.0 (16 abr) | v2.0 (23 abr) | Δ |
|---|---|---|---|
| Palabras | ~8.000 | ~14.300 | +79% |
| Secciones | 9 | 9 (misma estructura) | — |
| Diagramas | 0 | 12 SVG inline | +12 |
| Callouts | 0 | 4 tipos (DATO CLAVE, EJERCICIO, AYTO MADRID, REFERENCIA CRUZADA) | +4 |
| Ejemplos Ayto Madrid | 0 explícitos | 7 (Padrón, SIMA, Open Data, CMI alcalde, planificación urbana, etc.) | +7 |
| Fuentes Tier 1 | 9 | 18 | +9 |
| Nuevas subsecciones | — | 12 | +12 |
| Preguntas test | 15 | 25 (+10 nuevas) | +10 |
| Ficheros totales | 7 | 10 (+diagramas.md, +changelog.md, +piloto.pdf) | +3 |

---

## Cambios por sección

### Sección 1 — Dato e información

**Añadido**:
- Nueva subsección **1.3 Pirámide DIKW** con ejemplo Ayto Madrid + **diagrama D1** (SVG)
- Nueva subsección **1.4 Ciclo de vida del dato** (6 fases, tabla con ejemplos Ayto Madrid)
- Nueva subsección **1.5 Calidad del dato** (4 dimensiones canónicas + ISO 8000)
- Nueva subsección **1.6 Metadatos** (3 tipos + ejemplo Open Data Madrid DCAT-AP-ES)
- Ampliada **1.7 Clasificación de datos**: se añade clasificación por estructura (estructurado/semi/no-estructurado)

**Palabras**: 600 → 1.400 (+133%)

### Sección 2 — Sistemas de información

**Añadido**:
- **Diagrama D2** (Componentes SI, 7 bloques)
- **Diagrama D3** (Pirámide tipos SI con niveles organizacionales)
- Ampliada 2.3: referencia explícita a **tríada CIA** e **ISO 27001 / ENS Real Decreto 311/2022**
- Ampliada 2.6: ejemplo Ayto Madrid con Padrón como TPS, cuadro de mando del alcalde como EIS
- Nueva subsección **2.7 SI empresariales transversales** (ERP, CRM, SCM, BPM, BI, DWH)
- Ampliada 2.8: Data Lake y Data Lakehouse añadidos
- Nueva subsección **2.9 Metodologías de implantación** (Métrica v3, ITIL v4, COBIT, ágil)

**Palabras**: 1.200 → 2.200 (+83%)

### Sección 3 — Arquitectura de ordenadores

**Añadido**:
- **Diagrama D4** (Von Neumann vs Harvard side-by-side)
- Distinción **ISA vs organización** en preámbulo
- Referencia explícita a **First Draft of a Report on the EDVAC (1945)**
- Ampliada 3.2: referencia a Harvard Mark I (1944)
- Ampliada 3.3 Harvard modificada: detalle de cache L1 separada vs L2/L3 unificada en x86-64 y ARM

**Palabras**: 800 → 1.400 (+75%)

### Sección 4 — Generaciones de ordenadores

**Añadido**:
- **Diagrama D5** (Timeline horizontal con 5+1 generaciones)
- Datos concretos (tamaño ENIAC, consumo, fechas invención transistor con nombres Bardeen/Brattain/Shockley)
- Ejemplo Ayto Madrid: **IBM 650 RENFE 1959** como primer ordenador en España
- Nueva subsección **4.6 Sexta generación** (1991→actual): multinúcleo, cloud, móviles, IA, cuántica, neuromórfica

**Palabras**: 700 → 1.300 (+86%)

### Sección 5 — Componentes CPU

**Añadido** (sección con mayor ampliación):
- **Diagrama D6** (Bloques CPU con buses)
- **Diagrama D7** (Ciclo Fetch-Execute de 7 pasos)
- **Diagrama D8** (Modos de direccionamiento con ejemplos)
- Ampliada 5.2.1 CISC vs RISC con ejemplos modernos (Apple M4, AWS Graviton, RISC-V)
- Nueva subsección **5.2.4 Pipelining** (5 etapas RISC, hazards, forwarding, branch prediction)
- Nueva subsección **5.2.5 CPU superescalar**
- Nueva subsección **5.2.6 Ley de Moore y su crisis**
- Nueva subsección **5.2.7 Procesadores actuales** (Intel, AMD, Apple, Qualcomm, NVIDIA, AWS)
- Nueva subsección **5.3.1.1 FLAGS, EFLAGS, RFLAGS** (x86) — detalle bits principales + ejemplo
- Ampliada 5.5 Modos de direccionamiento: modos adicionales (pre/post-indexado, base-desplazamiento-escala x86, relativo a PC)
- Mnemónicos de instrucciones en **castellano** (`SUMA A, B`, `COMPARA A, B`, `SALTA_SI_IGUAL`, `INC A`)
- Ejemplo resuelto sobre flags con ADD/SUMA

**Palabras**: 2.400 → 4.500 (+87%)

### Sección 6 — Memoria

**Añadido**:
- **Diagrama D9** (Jerarquía de memoria con latencias y tamaños)
- **Diagrama D10** (Evolución RAM con barras comparativas hasta DDR5)
- **Diagrama D11** (BIOS vs UEFI comparativa)
- Tabla DDR actualizada: **incluye DDR5** (año, voltaje, frecuencia, ancho banda, capacidad, pines)
- Nueva subsección **6.2.8 Memoria virtual y paginación** (página, marco, TLB, fallo página, swap)
- Ampliada 6.2.4 Tipos especiales: LPDDR, HBM añadidos
- Nueva subsección **6.3.1 NAND Flash vs NOR Flash** (SLC, MLC, TLC, QLC)
- Ampliada 6.4: referencia TPM 2.0 y Windows 11, CSM

**Palabras**: 1.600 → 3.000 (+88%)

### Sección 7 — Medidas de capacidad

**Añadido**:
- Nueva subsección **7.1 IEC vs SI** (Kibi/Mebi/Gibi vs Kilo/Mega/Giga) con tabla comparativa
- Ejercicio resuelto: SSD 2 TB en Windows
- Nueva subsección **7.2 Volúmenes reales** con cifras de referencia

**Palabras**: 150 → 450 (+200%)

### Sección 8 — Sistemas de numeración

**Añadido**:
- Nueva subsección **8.1 Conversión entre bases** con 4 ejercicios resueltos (dec→bin, bin→dec, bin→hex, hex→bin)
- Nueva subsección **8.2 Complemento a 2** con ejercicio resuelto
- Nueva subsección **8.3 IEEE 754 coma flotante** con tabla de formatos

**Palabras**: 250 → 700 (+180%)

### Sección 9 — Juegos de caracteres

**Añadido**:
- **Diagrama D12** (Estructura UTF-8)
- Ampliada 9.1: tabla caracteres ASCII notables
- Nueva subsección **9.4 UTF-16 y UTF-32**
- Nueva subsección **9.5 BOM** (Byte Order Mark)
- Nueva subsección **9.6 Normalización Unicode** (NFC/NFD/NFKC/NFKD)
- Nueva subsección **9.8 ISO/IEC 10646**

**Palabras**: 700 → 1.400 (+100%)

---

## Elementos transversales nuevos

### Cajas callout (4 tipos)

Se introducen 4 tipos de callout reutilizables en todo el temario:

1. **[DATO CLAVE EXAMEN]** — alta densidad memorística (15 apariciones en el tema)
2. **[EJERCICIO RESUELTO]** — problema + solución paso a paso (7 apariciones)
3. **[EJEMPLO AYTO MADRID]** — aplicación real municipal (7 apariciones)
4. **[REFERENCIA CRUZADA]** — enlaces a otros temas (5 apariciones)

### Idioma del código

Cambio de mnemónicos: en v1.0 se mezclaban formas. En v2.0 se uniforma a **castellano** (`SUMA A, B`, `SALTA_SI_IGUAL`, `INC A`) según decisión de María. La nomenclatura de registros y estándares se mantiene en original (`MAR`, `MBR`, `CP`, `RI`, `FLAGS`, `EFLAGS`, `RFLAGS`).

---

## Ficheros afectados

| Fichero | Cambio |
|---|---|
| `tema-11-contenido.md` | Reescrito (8K → 14K palabras + 12 SVG) |
| `tema-11-indice.md` | Sin cambios (estructura no modificada) |
| `tema-11-fuentes.md` | Ampliado (9 → 18 fuentes Tier 1) |
| `tema-11-test.md` | Ampliado (15 → 25 preguntas) |
| `tema-11-caso-practico.md` | Sin cambios en esta iteración |
| `tema-11-validacion.md` | Actualizado checklist v2 |
| `tema-11-piloto.html` | Regenerado con 12 diagramas inyectados |
| `index.html` | Regenerado (copia de piloto.html) |
| **`tema-11-diagramas.md`** | **NUEVO** — catálogo SVG |
| **`tema-11-changelog.md`** | **NUEVO** — este fichero |
| **`tema-11-piloto.pdf`** | **NUEVO** — versión A4 light imprimible |

---

## Peticiones de María cubiertas

| Petición | Estado |
|---|---|
| Añadir diagramas al tema | Cubierto: 12 SVG inline, uno por bloque temático |
| Multiplicar por 2 el contenido | Cubierto parcialmente: 8K → 14.3K (+79%, focalizado en CPU y memoria según acuerdo) |
| Añadir ejemplos Ayto Madrid | Cubierto: 7 ejemplos (Padrón, SIMA, Open Data, CMI alcalde, etc.) |
| Cajas callout "Dato clave" y "Ejercicio resuelto" | Cubierto: 4 tipos de callout transversales |
| Ampliar profundidad técnica (FLAGS/EFLAGS/RFLAGS, modos direccionamiento, pipelining) | Cubierto: 5.2.4 Pipelining completo, 5.3.1.1 FLAGS completo, 5.5.1 modos adicionales |
| Versión PDF imprimible A4 light | Cubierto: tema-11-piloto.pdf |
| Mnemónicos en castellano | Cubierto: `SUMA A, B` en todo el documento |

---

## Pendientes post-v2.0

- Validación María/Ana del contenido ampliado
- Verificación de rigor técnico en nuevas subsecciones (pipelining, FLAGS, memoria virtual)
- Decidir si aplicar este patrón de ampliación a los 39 temas restantes
- Actualizar caso práctico (tema-11-caso-práctico.md) con escenario Ayto Madrid ampliado — pendiente decisión María
- Generar PDF con Puppeteer (pendiente de validación)

---

*Changelog generado como parte del pipeline v2.0 · MGS · 2026-04-23*
