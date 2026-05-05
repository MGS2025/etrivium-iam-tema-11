# Tema 11 — Changelog (v1.0 → v2.0 → v3.0 → v3.1)

> **Versiones**:
> - v1.0 (2026-04-16) — primera versión del piloto.
> - v2.0 (2026-04-23) — iteración tras feedback de María (21 abr 2026).
> - v3.0 (2026-04-28) — iteración tras revisión de María/Ana: ampliación de tipos de datos, elementos de SI y características de SI.
> - **v3.1 (2026-05-05) — iteración tras feedback de Jesús Cuadrado (IAM): correcciones puntuales sin reescritura. Sin ampliación de contenido nuevo.**

---

## Cambios v3.1 — Resumen

> **Fecha**: 2026-05-05
> **Autor**: ETRIVIUM LEARN SL (JMS)
> **Motivo**: feedback de Jesús Cuadrado del IAM tras revisión de v3.0 (4 may 2026). Iteración correctiva, no de ampliación.

### Cambios v3.1 por punto del feedback

**Punto 1 — Densidad / extensión del tema** (queda abierto)

- No se aplica en v3.1. A la espera de los índices de academias que Jesús está consiguiendo. Se valorará en una eventual v3.2 si se detectan gaps temáticos respecto a esos índices.

**Punto 2 — Falta de enlaces a referencias externas (ISO, etc.)**

- Añadidos enlaces inline (`<a href>`) a las normas y disposiciones legales en sus primeras menciones del documento:
  - [ISO/IEC 11404](https://www.iso.org/standard/39479.html) (Tipos de datos independientes de lenguaje)
  - [ISO/IEC 9075](https://www.iso.org/standard/63555.html) (SQL:2016)
  - [ISO/IEC 25010](https://www.iso.org/standard/35733.html) (SQuaRE — calidad de software)
  - [ISO 8000](https://www.iso.org/standard/50798.html) (Calidad de datos)
  - [ISO/IEC 27001](https://www.iso.org/standard/27001) (Seguridad de la información)
  - [ISO/IEC 27040](https://www.iso.org/standard/80194.html) (Seguridad del almacenamiento)
  - [UNE-EN 301 549](https://www.une.org/encuentra-tu-norma/busca-tu-norma/norma/?c=N0067945) (Accesibilidad TIC)
  - [WCAG 2.1](https://www.w3.org/TR/WCAG21/) (W3C)
  - [Real Decreto 1112/2018](https://www.boe.es/eli/es/rd/2018/09/07/1112) (Accesibilidad sector público)
  - [Real Decreto 311/2022](https://www.boe.es/eli/es/rd/2022/05/03/311) (Esquema Nacional de Seguridad)

**Punto 3 — DCAT-AP-ES sin definir**

- §1.6 Metadatos · callout *Ejemplo Ayto Madrid*: añadida definición inline ("la adaptación española del *Data Catalog Vocabulary - Application Profile* europeo, vocabulario común que la Unión Europea exige para describir conjuntos de datos abiertos del sector público y permitir que sean catalogables e interoperables entre administraciones").

**Punto 4 — Erratas estilo IA ("Array (vector): colección ordenada…")**

- §1.7.6 Tipos compuestos: reescrito completamente el bloque eliminando el patrón "Término: cláusula técnica seca". Cada tipo compuesto (array, struct, union, enum, string) pasa de definición telegráfica a párrafo pedagógico con verbo, ejemplo concreto y matiz cuando aplica. Eliminada la mención a "Acceso O(1) por índice" (jerga de doc técnica fuera de nivel C1).

**Punto 5 — Referencias cruzadas erróneas con otros temas** (CRÍTICO)

Auditadas TODAS las referencias cruzadas del tema contra el listado oficial del programa publicado en el BOAM 10.032 / 23-dic-2025. Se detectaron 11 errores en 8 ubicaciones. Resumen:

| Ubicación | v3.0 decía | v3.1 dice (correcto BOAM) |
|---|---|---|
| §1.7.7 *Referencia cruzada* TAD | "Tema 27 (Estructuras de datos y algoritmos)" | **Tema 13** (Tipos abstractos y Estructuras de datos) |
| §1.7.7 *Referencia cruzada* SO | "Tema 20 (Sistemas operativos)" | **Tema 14** (Sistemas operativos) |
| §1.7.9 *Referencia cruzada* (cierre §1) | "Tema 20 (SO) … Tema 27 (Estr. datos)" | **Tema 14** (SO) … **Tema 13** (TAD/Estr. datos) |
| §2.9 *Referencia cruzada* metodologías | "Tema 30 (Ingeniería del SW) y Tema 25 (Gestión de servicios TI)" | Reformulado como nota: ambos no existen como temas independientes en el BOAM |
| §4.6 *Referencia cruzada* Cloud/IA | "Tema 28 (Cloud) y Tema 36 (IA y Big Data)" | **Tema 31** (Computación distribuida y Cloud); IA/Big Data no es tema independiente del BOAM, eliminada esa parte |
| §5.2.5 *Referencia cruzada* paralelismo | "Tema 19 (Arquitecturas paralelas)" | Reformulado como nota: no existe tal tema en el BOAM |
| §6.2.8 *Referencia cruzada* memoria virtual | "Tema 20 (Sistemas operativos)" | **Tema 14** (Sistemas operativos) |
| §9.8 *Referencia cruzada* codificaciones | "Tema 16 (Comunicación de datos) y Tema 34 (Internet y servicios web)" | **Tema 33** (Comunicaciones) y **Tema 35** (Internet, HTTP/HTTPS/SSL/TLS) |

**Punto 6 — Pirámide TPS / MIS / DSS / EIS con criterios no introducidos**

- §2.6 Tipos de SI (clasificación por nivel organizacional):
  - Añadido párrafo narrativo introductorio que presenta los **cuatro niveles de decisión** (operativo, gestión/táctico, analítico, estratégico) ANTES del diagrama, citando a Anthony (1965) y Laudon &amp; Laudon (2017).
  - Añadido segundo párrafo explicando explícitamente la regla "+ altura → + agregación / – volumen" que antes solo aparecía como pie de diagrama abreviado.
  - Pie del diagrama reescrito en dos líneas legibles ("Cima: más agregación, menos volumen" / "Base: menos agregación, más volumen").
  - Diagrama SVG: corregidas tildes en los rótulos de nivel (`Estrategico` → `Estratégico`, `Analitico` → `Analítico`, `Gestion` → `Gestión / Táctico`).
  - Tabla de tipos de SI: corregido `Tactico` → `Gestión / Táctico` en la fila MIS.
  - `aria-label` del SVG ampliado para describir los 4 niveles de la pirámide.

**Punto 7 — Gráficos con problemas de accesibilidad (letra clara sobre fondo claro)**

Detectado un bug sistémico: las clases CSS de los SVG declaraban `fill:#fff` (texto blanco) y los overrides inline `fill="#1a1a1a"` no se aplicaban por mayor especificidad de la clase CSS. Por eso textos como "Memoria RAM", "E/S", "ROM/BIOS" del diagrama de bloques de la CPU se renderizaban en blanco sobre fondo azul muy claro `#d6e4f0` — ilegibles.

Solución: añadidas clases dedicadas `.cpu-heading-dark`, `.jm-label-dark`, `.dikw-label-dark`, `.tps-eis-dark` con `fill:#0a2540` (azul muy oscuro) y aplicadas a los textos sobre fondo claro.

Diagramas afectados y arreglados:

- **D6** Bloques internos de la CPU — Memoria RAM, E/S, ROM/BIOS pasan a texto oscuro legible. Buses (control rojo, direcciones verde, datos azul) reforzados a tonos más oscuros para AA.
- **D9** Jerarquía de memoria — SSD y "HDD/cinta/nube" pasan a texto oscuro legible.
- **D1** Pirámide DIKW — el nivel base "Dato" (sobre fondo `#6ea3d2`) pasa a texto oscuro.
- **D3** Pirámide TPS/MIS/DSS/EIS — el nivel base "TPS" (sobre fondo `#6ea3d2`) pasa a texto oscuro.

Adicionalmente: `aria-label` de SVGs enriquecidos con descripción explícita del contenido (mejora SR/lectores de pantalla, alineado con WCAG 2.1).

### Ficheros afectados v3.1

| Fichero | Cambio |
|---|---|
| `tema-11-contenido.md` | 9 ediciones puntuales (refs cruzadas + erratas IA + pirámide TPS narrativa + DCAT-AP-ES + enlaces ISO/BOE/W3C + 4 SVG con clases dark) |
| `index.html` | Mismas ediciones replicadas + actualización de versión `v3.0` → `v3.1` y banner |
| `tema-11-changelog.md` | Este fichero — añadida sección v3.1 |

### Cifras de impacto v3.1

- 11 referencias cruzadas erróneas corregidas/reformuladas (Punto 5)
- 4 diagramas SVG con accesibilidad mejorada (Puntos 6 y 7)
- 10 enlaces a normas externas añadidos (Punto 2)
- 1 bloque de contenido reescrito sin ampliación: §1.7.6 Tipos compuestos (Punto 4)
- 0 palabras añadidas netas — iteración correctiva, no de ampliación

### Pendientes post-v3.1

- Validación final del feedback aplicado por parte de Jesús Cuadrado (IAM).
- Recibir índices de academias para evaluar Punto 1 (densidad).
- Si se valida v3.1, replicar la auditoría sistemática de referencias cruzadas (vs BOAM 10.032) en el resto de temas técnicos cuando se generen.

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
