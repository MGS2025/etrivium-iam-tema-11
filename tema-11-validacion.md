# Tema 11 — Checklist de Validación v2.0

> **Revisor asignado**: María / Ana (bloque técnico)
> **Versión**: 2.0 (tras feedback 21 abr 2026)
> **Estado**: PENDIENTE
> **Fecha generación**: 2026-04-23

---

## 0. Verificación general de la iteración v2.0

### Peticiones de María cubiertas

- [ ] Los 12 diagramas SVG están presentes en el contenido y en el HTML del piloto
- [ ] El contenido se ha ampliado respecto a v1.0 (objetivo 14K-16K palabras, actual: 14.3K)
- [ ] La ampliación es focalizada (mas en CPU y memoria), NO uniforme x2
- [ ] Hay ejemplos Ayto Madrid en secciones clave (Padrón, SIMA, Open Data, etc.)
- [ ] Están presentes los 4 tipos de callout: DATO CLAVE EXAMEN, EJERCICIO RESUELTO, EJEMPLO AYTO MADRID, REFERENCIA CRUZADA
- [ ] Los mnemónicos de código están en castellano (`SUMA A, B`, `SALTA_SI_IGUAL`, etc.)
- [ ] Se ha ampliado la profundidad en FLAGS/EFLAGS/RFLAGS, modos de direccionamiento y pipelining
- [ ] Existe versión PDF A4 light imprimible (tema-11-piloto.pdf)

---

## 1. Validación del contenido teórico (v2.0)

### 1.1 Contenido nuevo de v2.0 — Exactitud técnica

- [ ] **DIKW**: atribución correcta a Ackoff (1989), niveles en orden correcto
- [ ] **Ciclo de vida del dato**: 6 fases canónicas correctas
- [ ] **Calidad del dato**: 4 dimensiones (exactitud, completitud, consistencia, oportunidad) alineadas con ISO 8000
- [ ] **Metadatos**: 3 tipos (descriptivos, estructurales, administrativos) correctos
- [ ] **Tríada CIA**: explicación correcta, referencia a ISO 27001 y ENS RD 311/2022
- [ ] **Ejemplos Ayto Madrid**: Padrón como TPS, planificación urbana como DSS, CMI Alcalde como EIS — verificar coherencia
- [ ] **Metodologías**: Metrica v3 sigue vigente en pliegos de contratacion pública (confirmar)
- [ ] **First Draft EDVAC 1945**: atribución correcta a Von Neumann
- [ ] **Harvard Mark I 1944**: anterior cronológicamente a Von Neumann (verificar no confusión)
- [ ] **Sexta generación**: tratamiento como extensión moderna (cloud, cuántica, neuromórfica) — aceptable para C1?
- [ ] **IBM 650 RENFE 1959**: primer ordenador en España — verificar dato histórico
- [ ] **Pipeline RISC 5 etapas**: IF-ID-EX-MEM-WB correcto
- [ ] **Hazards del pipeline**: estructural, datos, control — definiciones correctas
- [ ] **Spectre/Meltdown**: 2018, afectan a ejecución especulativa — verificar
- [ ] **Superescalar**: definición correcta, ejemplos actuales (Intel Golden Cove 6 inst/ciclo, Apple M3 8 inst/ciclo)
- [ ] **Ley de Moore**: Gordon Moore 1965, crisis desde ~2015 — datos correctos
- [ ] **Procesadores actuales 2024**: Intel Core Ultra, AMD Ryzen 9000, Apple M4, Snapdragon X Elite, Graviton 4 — vigencia de modelos
- [ ] **Registros FLAGS**: bits correctos (CF=0, PF=2, ZF=6, SF=7, OF=11)
- [ ] **EFLAGS vs RFLAGS**: 32 vs 64 bits, retrocompatibilidad — correcto
- [ ] **Modos direccionamiento ampliados**: pre/post-indexado, base-desplaz-escala x86, relativo PC — correctos
- [ ] **DDR5**: 2021, 1,1 V, hasta 8400 MT/s, 128 GB/módulo — spec JEDEC JESD79-5 correcta
- [ ] **NAND vs NOR Flash**: tabla comparativa correcta
- [ ] **SLC/MLC/TLC/QLC**: bits por celda y durabilidad
- [ ] **Memoria virtual**: página (4 KB), marco, TLB, MMU, fallo página — coherente
- [ ] **LPDDR, HBM**: casos de uso correctos
- [ ] **TPM 2.0 / Windows 11**: obligatorio — correcto
- [ ] **Codepages 437, 850, 1252, ISO 8859-1, ISO 8859-15**: correctos
- [ ] **UTF-16 BE/LE, BOM**: códigos FEFF, FFFE correctos
- [ ] **Normalización Unicode NFC/NFD/NFKC/NFKD**: correcto
- [ ] **IEEE 754 single (1+8+23), double (1+11+52)**: correctos
- [ ] **Complemento a 2 8 bits rango**: -128 a +127 correcto
- [ ] **Ejercicios resueltos**: cálculos matemáticos correctos (25→11001, -5→11111011, etc.)

### 1.2 Contenido base de v1.0 — Exactitud técnica

- [ ] Definiciones de dato/información correctas y coherentes con ISO 2382
- [ ] Componentes de un SI completos y sin omisiones
- [ ] Arquitectura Von Neumann: cuello de botella descrito correctamente
- [ ] Arquitectura Harvard: separacion memoria datos/instrucciones OK
- [ ] Harvard modificada: concepto correcto, aplicación en x86-64 y ARM
- [ ] Generaciones de ordenadores: fechas, tecnologías y ejemplos correctos
- [ ] CISC vs RISC: comparativa correcta, x86 traduce a micro-RISC internamente
- [ ] Registros de la CPU: tipos y funciones correctas
- [ ] Fórmula 2^n para capacidad direccionamiento del MAR — correcta
- [ ] Ciclo instrucción: fases FETCH (1-5) y EXECUTE (6-7) descritas correctamente
- [ ] Modos direccionamiento impropios (implícito, inmediato) y propios (directo, indirecto, relativo, indexado) — definiciones correctas
- [ ] Tabla DDR (frecuencias, pines, capacidad) — contrastar con specs JEDEC
- [ ] ECC vs No-ECC: descripción correcta
- [ ] SRAM vs DRAM: basada en biestables / condensadores — correcto
- [ ] BIOS vs UEFI: 4 particiones MBR vs 128 GPT, Secure Boot, 16 vs 32/64 bits
- [ ] Tabla medidas capacidad: KB=1024, MB=1024KB... hasta YB — correcto
- [ ] ASCII: 7 bits, 128 caracteres, 1963 — verificar
- [ ] UTF-8: 1-4 bytes, compatible ASCII, autosincronización — correcto
- [ ] EBCDIC: 8 bits, IBM, mainframes — correcto

### 1.3 Nivel adecuado a C1

- [ ] No excede nivel técnico esperado para Técnico Auxiliar (no es ingeniero)
- [ ] Pipelining (sección 5.2.4): la profundidad es adecuada o excesiva?
- [ ] FLAGS/EFLAGS/RFLAGS (5.3.1.1): detalle adecuado tras ampliación de María?
- [ ] Modos direccionamiento ampliados (5.5.1): adecuados o excesivos?
- [ ] Memoria virtual (6.2.8): profundidad correcta o hay que recortar?
- [ ] IEEE 754 (8.3): adecuado para C1?
- [ ] Operaciones lógicas (tablas de verdad): necesarias o excesivas?

### 1.4 Coherencia interna

- [ ] No hay contradicciones entre secciones (v1 + v2)
- [ ] Terminologia consistente en todo el documento
- [ ] Las referencias cruzadas internas son correctas
- [ ] Los mnemónicos de código están **uniformemente en castellano** (no mezcla con inglés salvo nombres propios)

---

## 2. Validación de los diagramas (12 SVG)

### 2.1 Precision técnica de cada diagrama

- [ ] **D1 Pirámide DIKW**: 4 niveles correctos, ejemplo Ayto Madrid plausible
- [ ] **D2 Componentes SI**: 7 componentes correctos, agrupacion tecnología/humano/flujo aceptable
- [ ] **D3 Pirámide tipos SI**: TPS-MIS-DSS-EIS orden correcto, correspondencia con niveles organizacionales
- [ ] **D4 Von Neumann vs Harvard**: comparativa clara, cuello de botella señalado correctamente
- [ ] **D5 Timeline generaciones**: fechas y tecnologías correctas, 6ª generación como extensión visual
- [ ] **D6 Bloques CPU**: ALU, UC, Registros correctamente agrupados, 3 buses externos
- [ ] **D7 Ciclo Fetch-Execute**: 7 pasos correctos, separacion FETCH/EXECUTE clara
- [ ] **D8 Modos direccionamiento**: 5 modos con mismo operando (42), flujos correctos
- [ ] **D9 Jerarquía memoria**: 7 niveles correctos, latencias y tamaños realistas
- [ ] **D10 Evolucion RAM**: secuencia cronológica correcta, proporciones visuales adecuadas
- [ ] **D11 BIOS vs UEFI**: 8 aspectos comparados correctamente
- [ ] **D12 Estructura UTF-8**: bits de cabecera correctos (0xxx, 110xx, 1110xx, 11110xx)

### 2.2 Aspectos visuales y de usabilidad

- [ ] Los SVG son legibles a tamaño pantalla y A4 impreso
- [ ] Los colores (azul Ayto #0055a0 + verde + rojo + naranja) son accesibles (contraste WCAG AA)
- [ ] El texto dentro de los SVG es comprensible sin necesidad de zoom
- [ ] Los SVG se renderizan correctamente en el HTML del piloto
- [ ] Los SVG se renderizan correctamente en el PDF A4 light (si procede)
- [ ] Los SVG mantienen calidad al imprimir

---

## 3. Validación del test (25 preguntas)

### Formato

- [ ] Todas las preguntas tienen exactamente 3 opciones (A/B/C)
- [ ] Solo una respuesta correcta por pregunta
- [ ] Enunciados claros y sin ambigüedad
- [ ] Las opciones incorrectas son plausibles (no obvias)

### Correspondencia con el temario

- [ ] Cada pregunta se puede justificar con contenido del tema-11-contenido.md
- [ ] La referencia a sección/fuente es correcta en cada pregunta
- [ ] Distribución equilibrada entre las 9 secciones del tema
- [ ] Las 10 preguntas nuevas (P16-P25) cubren contenido ampliado en v2.0

### Dificultad

- [ ] Adecuada para nivel C1
- [ ] Mezcla de preguntas de memoria (datos concretos) y comprensión (conceptos)
- [ ] Ninguna pregunta es trivial ni excesivamente dificil

### Preguntas nuevas v2.0

- [ ] P16 (DIKW): enunciado y opción correcta correctos
- [ ] P17 (Calidad dato): 4 dimensiones ISO 8000 — opción correcta
- [ ] P18 (Padrón = TPS): ejemplo Ayto Madrid valido
- [ ] P19 (Pipeline 5 etapas): correcto
- [ ] P20 (ZF = resultado cero): correcto
- [ ] P21 (Complemento 2 8 bits = -128 a +127): correcto
- [ ] P22 (IEEE 754 single = 1+8+23): correcto
- [ ] P23 (UTF-8 BMP = 3 bytes): correcto
- [ ] P24 (MMU traduce): correcto
- [ ] P25 (Secure Boot verifica firma): correcto

---

## 4. Validación del caso práctico

- [ ] El supuesto es realista para el contexto del Ayuntamiento de Madrid
- [ ] Las especificaciones técnicas son actuales y coherentes
- [ ] Las cuestiones cubren diferentes secciones del tema
- [ ] Las respuestas orientativas son correctas y completas
- [ ] La puntuacion (10 puntos) está bien distribuida según dificultad
- [ ] Considerar si procede actualizar el caso con el contenido ampliado (pipelining, memoria virtual, FLAGS...)

---

## 5. Validación de fuentes (v2.0)

### Fuentes Tier 1 existentes (v1.0)

- [ ] Todas las fuentes Tier 1 listadas existen y están vigentes
- [ ] Las referencias [STALLINGS-COA, Cap. X] son correctas para la edicion citada
- [ ] Los datos JEDEC de DDR coinciden con las tablas del temario
- [ ] La especificación UEFI 2.10 está vigente
- [ ] RFC-20 (ASCII) es la referencia correcta

### Fuentes nuevas añadidas (v2.0)

- [ ] **ISO-11179** (metadatos): referencia correcta
- [ ] **ISO-8000** (calidad dato): referencia correcta
- [ ] **PATTERSON-HENNESSY** (pipelining): 6ª edicion 2020 correcta
- [ ] **ARM-ARM** (ARMv9-A): referencia correcta
- [ ] **IEEE-754 (2019)**: revisión actual
- [ ] **ISO-10646**: versión 2020 correcta
- [ ] **ENS-RD311**: Real Decreto 311/2022 vigente
- [ ] **RGPD**: Reglamento (UE) 2016/679 correcto
- [ ] **METRICA-V3**: sigue vigente en pliegos públicos
- [ ] **LAUDON-MIS**: 17ª edicion 2021 correcta
- [ ] **ACKOFF-DIKW**: referencia 1989 correcta
- [ ] **KAPLAN-BSC**: Harvard Business Review 1992 correcta
- [ ] **DATOS-MADRID**: portal Open Data vigente
- [ ] **IDC-DATA-SPHERE**: cifras 2025 actualizadas

---

## 6. Comparación con material existente

- [ ] El nuevo contenido **cubre TODO** lo que ya tenia el DOCX original (no se ha perdido nada)
- [ ] La estructura es más clara y navegable que el DOCX
- [ ] Se han añadido mejoras sustanciales (diagramas, callouts, ejemplos Ayto, ampliación pipelining/FLAGS)
- [ ] La extensión duplicada (x1.8) es proporcional al valor aportado (no relleno)

---

## 7. Validación del HTML del piloto

- [ ] Los 12 SVG se renderizan correctamente en el HTML
- [ ] Las 6 pestañas (Contenido / Índice / Test / Caso Práctico / Fuentes / Validación) siguen operativas
- [ ] El test interactivo corrige correctamente las 25 preguntas
- [ ] El branding Ayuntamiento de Madrid (#0055a0) se mantiene
- [ ] El HTML se abre correctamente en navegadores modernos (Chrome, Firefox, Safari, Edge)
- [ ] El HTML es responsive (móvil, tablet, desktop)
- [ ] El HTML es imprimible con estilos adecuados

---

## 8. Validación del PDF A4 light

- [ ] El PDF se genera correctamente desde el HTML (Puppeteer o similar)
- [ ] Fondo blanco, legible en impresion
- [ ] Los 12 SVG se ven con calidad suficiente
- [ ] Margenes A4 correctos (2,5 cm típicos)
- [ ] Header con título del tema en cada página
- [ ] Footer con numero de página
- [ ] Saltos de página razonables (no cortan tablas ni diagramas en medio)
- [ ] Tamaño aproximado del PDF: 30-50 páginas

---

## Resultado de la validación

| Aspecto | Resultado | Notas |
|---|---|---|
| Peticiones María cubiertas | PENDIENTE | |
| Exactitud contenido v2.0 | PENDIENTE | |
| Diagramas 12 SVG | PENDIENTE | |
| Test 25 preguntas | PENDIENTE | |
| Caso práctico | PENDIENTE | |
| Fuentes v2.0 | PENDIENTE | |
| HTML piloto | PENDIENTE | |
| PDF A4 light | PENDIENTE | |

**Validado por**: _______________
**Fecha**: _______________
**Decisión**: [ ] APROBADO · [ ] REQUIERE CAMBIOS · [ ] RECHAZADO

**Feedback adicional**:
```
(escribir aqui cualquier comentario, sugerencia o peticion de cambio)
```

---

*Checklist v2.0 generada automáticamente como parte del pipeline de producción MGS · 2026-04-23*
*Referencia pliego: sección 3.3 — Revisión y aprobación*
