# Tema 11 — Test de Autoevaluación

> **Título**: Informática básica. Representación y comunicación de la información.
> **Formato**: 25 preguntas tipo test A/B/C (formato oficial oposicion)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid
> **Versión**: 2.0 — 25 preguntas (15 base v1.0 + 10 nuevas v2.0)
> **Fecha**: 2026-04-23
> **Fuentes**: ver tema-11-fuentes.md

---

## Instrucciones

- Cada pregunta tiene **3 opciones** (A, B, C). Solo una es correcta.
- Penalización en examen real: respuesta incorrecta descuenta 1/3 del valor de una correcta.
- Tiempo orientativo: 1 minuto por pregunta.
- Las preguntas **P16-P25** cubren el contenido ampliado en v2.0 (DIKW, pipelining, FLAGS, IEEE 754, UTF-8, memoria virtual, ejemplos Ayto Madrid).

---

### Pregunta 1

**¿Cuál es la unidad mínima de información en un sistema informático?**

A) Byte
B) Bit
C) Nibble

<details>
<summary>Respuesta</summary>

**Correcta: B) Bit**

El bit (binary digit) es la unidad mínima de información, representando un valor binario (0 o 1). Un byte está compuesto por 8 bits, y un nibble por 4 bits.

*Referencia: tema-11-contenido.md, sección 7 — Medidas de capacidad [ISO-2382]*
</details>

---

### Pregunta 2

**¿En la arquitectura Von Neumann, cuál es la causa principal de su cuello de botella?**

A) La ALU no puede realizar operaciones aritméticas y lógicas simultáneamente
B) Los datos y las instrucciones comparten el mismo bus de memoria
C) La Unidad de Control no puede decodificar más de una instrucción a la vez

<details>
<summary>Respuesta</summary>

**Correcta: B) Los datos y las instrucciones comparten el mismo bus de memoria**

El cuello de botella de Von Neumann se produce porque datos e instrucciones comparten un único bus, impidiendo la búsqueda simultánea de instrucciones y datos. La arquitectura Harvard resuelve esto con buses separados.

*Referencia: tema-11-contenido.md, sección 3.1 [STALLINGS-COA, Cap. 2]*
</details>

---

### Pregunta 3

**¿Qué característica diferencia fundamentalmente la arquitectura Harvard de la Von Neumann?**

A) Harvard utiliza microprocesadores RISC exclusivamente
B) Harvard separa la memoria de instrucciones de la memoria de datos
C) Harvard no utiliza buses de control

<details>
<summary>Respuesta</summary>

**Correcta: B) Harvard separa la memoria de instrucciones de la memoria de datos**

La arquitectura Harvard divide la memoria principal en memoria de instrucciones y memoria de datos, cada una con su propio bus, permitiendo acceso simultáneo y eliminando el cuello de botella de Von Neumann.

*Referencia: tema-11-contenido.md, sección 3.2 [STALLINGS-COA, Cap. 2]*
</details>

---

### Pregunta 4

**¿Cuál de las siguientes afirmaciones sobre los procesadores RISC es correcta?**

A) Utilizan instrucciones complejas que requieren entre 4 y 10 ciclos de reloj
B) Solo las instrucciones de carga y almacenamiento acceden a la memoria de datos
C) Son la arquitectura predominante en los ordenadores de escritorio x86

<details>
<summary>Respuesta</summary>

**Correcta: B) Solo las instrucciones de carga y almacenamiento acceden a la memoria de datos**

Esta es una característica fundamental de RISC (arquitectura load-store). La opción A describe CISC (4-10 ciclos). La opción C es incorrecta: x86 es CISC (aunque internamente traduce a microinstrucciones RISC). Ejemplos RISC: ARM, MIPS, SPARC, RISC-V.

*Referencia: tema-11-contenido.md, sección 5.2.1 [STALLINGS-COA, Cap. 15]*
</details>

---

### Pregunta 5

**¿Qué componente de la CPU contiene la dirección de la siguiente instrucción a ejecutar?**

A) Registro de Instrucción (RI)
B) Contador de Programa (CP)
C) Registro de Estado (FLAGS)

<details>
<summary>Respuesta</summary>

**Correcta: B) Contador de Programa (CP)**

El Contador de Programa contiene en todo momento la dirección de memoria de la siguiente instrucción a ejecutar. El RI contiene la instrucción en ejecución. FLAGS almacena condiciones de la última operación.

*Referencia: tema-11-contenido.md, sección 5.3.2 [STALLINGS-COA, Cap. 20]*
</details>

---

### Pregunta 6

**¿Cuántos bytes componen un Kibibyte (KiB) según la norma IEC 60027-2?**

A) 1.000 bytes
B) 1.024 bytes
C) 512 bytes

<details>
<summary>Respuesta</summary>

**Correcta: B) 1.024 bytes**

Según la norma IEC 60027-2, 1 KiB (kibibyte) = 2^10 = 1.024 bytes. El prefijo KB (kilobyte) corresponde al sistema decimal SI (1.000 bytes), usado por fabricantes de discos duros para expresar capacidades comerciales.

*Referencia: tema-11-contenido.md, sección 7.1 [IEC 60027-2]*
</details>

---

### Pregunta 7

**¿En la primera generación de ordenadores (1940-1952), cual era el componente electrónico principal?**

A) Transistores
B) Circuitos integrados
C) Válvulas de vacío

<details>
<summary>Respuesta</summary>

**Correcta: C) Válvulas de vacío**

La primera generación utilizaba válvulas y tubos de vacío (ENIAC, Mark I, UNIVAC I). Los transistores corresponden a la segunda generación (1952-1964) y los circuitos integrados a la tercera (1964-1970).

*Referencia: tema-11-contenido.md, sección 4.1 [TANENBAUM-SO, Cap. 1]*
</details>

---

### Pregunta 8

**¿Qué tipo de bus transporta las direcciones de memoria sobre las que se va a actuar en operaciones de lectura y escritura?**

A) Bus de datos
B) Bus de control
C) Bus de direcciones

<details>
<summary>Respuesta</summary>

**Correcta: C) Bus de direcciones**

El bus de direcciones transporta las direcciones de memoria. El bus de datos traslada los datos. El bus de control transmite señales de la Unidad de Control. El bus de direcciones es unidireccional (CPU → memoria).

*Referencia: tema-11-contenido.md, sección 5.1 [STALLINGS-COA, Cap. 3]*
</details>

---

### Pregunta 9

**¿Qué tipo de memoria ROM puede borrarse mediante exposicion a luz ultravioleta y reprogramarse eléctricamente?**

A) PROM
B) EPROM
C) EEPROM

<details>
<summary>Respuesta</summary>

**Correcta: B) EPROM**

La EPROM (Erasable Programmable ROM) se borra mediante luz ultravioleta (ventana de cuarzo) y se programa eléctricamente. La PROM solo puede programarse una vez. La EEPROM se borra y reprograma eléctricamente sin necesidad de luz ultravioleta.

*Referencia: tema-11-contenido.md, sección 6.3*
</details>

---

### Pregunta 10

**¿Cuál de las siguientes NO es una función básica de un sistema de información?**

A) Procesamiento de información
B) Compilación de código fuente
C) Almacenamiento de información

<details>
<summary>Respuesta</summary>

**Correcta: B) Compilación de código fuente**

Las 4 funciones básicas de un SI (regla nemotécnica EAPS) son: Entrada, Almacenamiento, Procesamiento y Salida de información. La compilación de código fuente es una función específica de herramientas de desarrollo, no generica de un SI.

*Referencia: tema-11-contenido.md, sección 2.5*
</details>

---

### Pregunta 11

**¿Cuántos pines tienen los módulos de memoria DDR4?**

A) 240 pines
B) 184 pines
C) 288 pines

<details>
<summary>Respuesta</summary>

**Correcta: C) 288 pines**

DDR4 tiene 288 pines, al igual que DDR5 (aunque con voltajes distintos: 1,2 V vs 1,1 V, incompatibles). DDR tiene 184 pines. DDR2 y DDR3 comparten 240 pines pero con la muesca en diferente posición (incompatibles entre sí).

*Referencia: tema-11-contenido.md, sección 6.2.3 [JEDEC JESD79-4]*
</details>

---

### Pregunta 12

**¿Que codificación de caracteres utiliza entre 1 y 4 bytes por carácter y es compatible con ASCII de 7 bits?**

A) EBCDIC
B) UTF-8
C) ISO-8859-1

<details>
<summary>Respuesta</summary>

**Correcta: B) UTF-8**

UTF-8 utiliza longitud variable (1-4 bytes) y es plenamente compatible con US-ASCII de 7 bits (los primeros 128 code points coinciden). EBCDIC es un código de 8 bits de IBM no compatible con ASCII. ISO-8859-1 (Latin-1) usa 8 bits fijos.

*Referencia: tema-11-contenido.md, sección 9.3 [UNICODE-STD]*
</details>

---

### Pregunta 13

**¿Qué tecnología permite a un núcleo de procesador ejecutar dos tareas simultáneas?**

A) Multiprocesamiento
B) MultiThreading (HyperThreading / SMT)
C) Multinúcleo

<details>
<summary>Respuesta</summary>

**Correcta: B) MultiThreading (HyperThreading / SMT)**

El MultiThreading duplica las unidades lógicas de cada núcleo, permitiendo dos hilos simultáneos por núcleo. Intel lo denomina HyperThreading y AMD lo denomina SMT. El multiprocesamiento implica multiples CPUs físicas. Multinúcleo significa multiples núcleos físicos en un mismo chip.

*Referencia: tema-11-contenido.md, sección 5.2.3*
</details>

---

### Pregunta 14

**¿Cuál de las siguientes diferencias entre UEFI y BIOS es correcta?**

A) BIOS soporta hasta 128 particiones GPT por disco, UEFI solo 4 particiones MBR
B) UEFI se ejecuta en 16 bits, igual que BIOS
C) UEFI soporta hasta 128 particiones GPT por disco, mientras que BIOS se limita a 4 particiones MBR

<details>
<summary>Respuesta</summary>

**Correcta: C) UEFI soporta hasta 128 particiones GPT por disco, mientras que BIOS se limita a 4 particiones MBR**

UEFI permite 128 particiones GPT (hasta 8 ZB) frente a las 4 particiones MBR de BIOS (hasta 2,2 TB). UEFI se ejecuta en 32 o 64 bits, no en 16. La opción A invierte los datos.

*Referencia: tema-11-contenido.md, sección 6.4 [UEFI-SPEC]*
</details>

---

### Pregunta 15

**¿En el ciclo de ejecución de instrucciones, que ocurre durante la fase de búsqueda (FETCH)?**

A) La ALU ejecuta la operación aritmética correspondiente
B) La instrucción es localizada en memoria y transferida al Registro de Instrucción
C) El Contador de Programa se decrementa para apuntar a la instrucción anterior

<details>
<summary>Respuesta</summary>

**Correcta: B) La instrucción es localizada en memoria y transferida al Registro de Instrucción**

En la fase FETCH: (1) el CP transfiere la dirección al MAR, (2) MAR emite dirección a memoria, (3) la memoria entrega la instrucción al MBR, (4) se transfiere al RI, (5) CP se incrementa. La ejecución de operaciones por la ALU corresponde a la fase EXECUTE.

*Referencia: tema-11-contenido.md, sección 5.4 [STALLINGS-COA, Cap. 12]*
</details>

---

## Preguntas nuevas v2.0 (contenido ampliado)

### Pregunta 16

**¿En la pirámide DIKW, cuál es el orden correcto de los niveles, de abajo a arriba?**

A) Dato → Conocimiento → Información → Sabiduría
B) Dato → Información → Conocimiento → Sabiduría
C) Información → Dato → Sabiduría → Conocimiento

<details>
<summary>Respuesta</summary>

**Correcta: B) Dato → Información → Conocimiento → Sabiduría**

La pirámide DIKW (Data-Information-Knowledge-Wisdom), atribuida a Russell Ackoff (1989), ordena de base a cima: Dato (hechos brutos), Información (datos con contexto), Conocimiento (patrones y relaciones), Sabiduría (decisiones fundamentadas).

*Referencia: tema-11-contenido.md, sección 1.3 [ACKOFF-DIKW]*
</details>

---

### Pregunta 17

**¿Cuáles son las cuatro dimensiones canónicas de calidad del dato según ISO 8000?**

A) Exactitud, Completitud, Consistencia, Oportunidad
B) Seguridad, Privacidad, Confidencialidad, Integridad
C) Velocidad, Precision, Exactitud, Relevancia

<details>
<summary>Respuesta</summary>

**Correcta: A) Exactitud, Completitud, Consistencia, Oportunidad**

Las cuatro dimensiones canónicas son exactitud (accuracy), completitud (completeness), consistencia (consistency) y oportunidad (timeliness). ISO 8000 amplía a 10+ dimensiones (unicidad, validez, precision, etc.).

*Referencia: tema-11-contenido.md, sección 1.5 [ISO-8000]*
</details>

---

### Pregunta 18

**¿En el sistema de información del Ayuntamiento de Madrid, el Padrón Municipal corresponde principalmente a que tipo de sistema?**

A) EIS (Executive Information System)
B) DSS (Decisión Support System)
C) TPS (Transaction Processing System)

<details>
<summary>Respuesta</summary>

**Correcta: C) TPS (Transaction Processing System)**

El Padrón Municipal gestiona transacciones diarias de altas, bajas y modificaciones de residentes en tiempo real. Alimenta un MIS estadístico y, a nivel superior, nutre DSS de planificación y EIS del cuadro de mando del Alcalde.

*Referencia: tema-11-contenido.md, sección 2.6 — Ejemplo Ayto Madrid*
</details>

---

### Pregunta 19

**¿Cuántas etapas tiene el pipeline RISC clásico (modelo MIPS)?**

A) 3 etapas
B) 5 etapas
C) 7 etapas

<details>
<summary>Respuesta</summary>

**Correcta: B) 5 etapas**

El pipeline RISC clásico tiene 5 etapas: IF (Instruction Fetch), ID (Instruction Decode), EX (Execute), MEM (Memory Access), WB (Write Back). Procesadores modernos pueden tener 15-19 etapas.

*Referencia: tema-11-contenido.md, sección 5.2.4 [PATTERSON-HENNESSY]*
</details>

---

### Pregunta 20

**¿En el registro FLAGS de arquitectura x86, que indica el bit ZF (Zero Flag)?**

A) El resultado de la última operación es cero
B) El procesador está en modo protegido
C) Se ha producido un desbordamiento en la operación

<details>
<summary>Respuesta</summary>

**Correcta: A) El resultado de la última operación es cero**

El bit ZF (Zero Flag, bit 6 del registro FLAGS) se activa cuando el resultado de una operación aritmética o lógica es cero. Se utiliza en saltos condicionales como `SALTA_SI_IGUAL` (equivalente a `JE`/`JZ` en x86). El desbordamiento con signo lo indica OF.

*Referencia: tema-11-contenido.md, sección 5.3.1.1 [INTEL-SDM]*
</details>

---

### Pregunta 21

**¿Cuál es el rango de valores que puede representar un numero entero de 8 bits en complemento a 2?**

A) De 0 a 255
B) De -127 a +127
C) De -128 a +127

<details>
<summary>Respuesta</summary>

**Correcta: C) De -128 a +127**

En complemento a 2 con 8 bits, el rango es -2^(n-1) a +2^(n-1)-1 = -128 a +127. El cero tiene una unica representación (todos bits a 0), a diferencia del complemento a 1. La opción A es sin signo (0-255), la B omite el -128.

*Referencia: tema-11-contenido.md, sección 8.2*
</details>

---

### Pregunta 22

**¿En el formato IEEE 754 de precision simple (float 32 bits), cuál es la distribución de bits?**

A) 1 bit signo, 8 bits exponente, 23 bits mantisa
B) 1 bit signo, 11 bits exponente, 20 bits mantisa
C) 2 bits signo, 7 bits exponente, 23 bits mantisa

<details>
<summary>Respuesta</summary>

**Correcta: A) 1 bit signo, 8 bits exponente, 23 bits mantisa**

IEEE 754 precision simple (single, 32 bits) = 1 + 8 + 23. Doble precision (64 bits) = 1 + 11 + 52. La opción B corresponde parcialmente a doble precision pero con mantisa incorrecta.

*Referencia: tema-11-contenido.md, sección 8.3 [IEEE-754]*
</details>

---

### Pregunta 23

**¿Cuántos bytes utiliza UTF-8 para codificar un carácter del BMP (Basic Multilingual Plane) que incluye CJK?**

A) 1 byte
B) 2 bytes
C) 3 bytes

<details>
<summary>Respuesta</summary>

**Correcta: C) 3 bytes**

UTF-8 usa 1 byte para ASCII (U+0000-U+007F), 2 bytes para Latin extendido (U+0080-U+07FF), **3 bytes para el BMP completo incluyendo CJK** (U+0800-U+FFFF), y 4 bytes para planos suplementarios (U+10000+, incluye emojis).

*Referencia: tema-11-contenido.md, sección 9.3 [UNICODE-STD]*
</details>

---

### Pregunta 24

**¿Qué componente hardware de la CPU traduce direcciones virtuales a direcciones físicas en un sistema con memoria virtual?**

A) TLB (Translation Lookaside Buffer) de forma autónoma
B) MMU (Memory Management Unit) consultando la tabla de páginas
C) La ALU mediante operaciones aritméticas

<details>
<summary>Respuesta</summary>

**Correcta: B) MMU (Memory Management Unit) consultando la tabla de páginas**

La MMU es el hardware dentro de la CPU responsable de la traducción dirección virtual → física. Consulta la tabla de páginas. El TLB es una **cache** de traducciones recientes que acelera a la MMU, pero no traduce por sí solo (es solo memoria, no lógica).

*Referencia: tema-11-contenido.md, sección 6.2.8 [TANENBAUM-SO]*
</details>

---

### Pregunta 25

**¿Cuál de estas afirmaciones sobre el Secure Boot de UEFI es correcta?**

A) Cifra el disco duro automáticamente al iniciar el sistema
B) Verifica la firma digital del bootloader antes de ejecutarlo para impedir rootkits
C) Requiere siempre un chip TPM 3.0 o superior

<details>
<summary>Respuesta</summary>

**Correcta: B) Verifica la firma digital del bootloader antes de ejecutarlo para impedir rootkits**

Secure Boot es una funcionalidad de UEFI que verifica la firma digital del bootloader (y opcionalmente del kernel) antes de ejecutarlo, impidiendo el arranque de bootkits y malware previo al SO. Es obligatorio para Windows 11. No cifra el disco (eso es BitLocker/LUKS). TPM 2.0 es lo exigido por Windows 11.

*Referencia: tema-11-contenido.md, sección 6.4 [UEFI-SPEC]*
</details>

---

## Resumen de resultados

| # | Correcta | Sección | Tipo |
|---|---|---|---|
| 1 | B | 7 Medidas capacidad | Base |
| 2 | B | 3.1 Von Neumann | Base |
| 3 | B | 3.2 Harvard | Base |
| 4 | B | 5.2.1 CISC/RISC | Base |
| 5 | B | 5.3.2 UC | Base |
| 6 | B | 7.1 IEC vs SI | Base |
| 7 | C | 4.1 Primera generación | Base |
| 8 | C | 5.1 Buses | Base |
| 9 | B | 6.3 ROM | Base |
| 10 | B | 2.5 Funciones SI | Base |
| 11 | C | 6.2.3 DDR | Base |
| 12 | B | 9.3 UTF-8 | Base |
| 13 | B | 5.2.3 Multithreading | Base |
| 14 | C | 6.4 BIOS/UEFI | Base |
| 15 | B | 5.4 Ciclo instrucción | Base |
| **16** | **B** | **1.3 DIKW** | **Nueva v2** |
| **17** | **A** | **1.5 Calidad dato** | **Nueva v2** |
| **18** | **C** | **2.6 Ayto Madrid** | **Nueva v2** |
| **19** | **B** | **5.2.4 Pipelining** | **Nueva v2** |
| **20** | **A** | **5.3.1.1 FLAGS** | **Nueva v2** |
| **21** | **C** | **8.2 Complemento 2** | **Nueva v2** |
| **22** | **A** | **8.3 IEEE 754** | **Nueva v2** |
| **23** | **C** | **9.3 UTF-8 BMP** | **Nueva v2** |
| **24** | **B** | **6.2.8 MMU** | **Nueva v2** |
| **25** | **B** | **6.4 Secure Boot** | **Nueva v2** |

**Distribución por sección** (v2.0, 25 preguntas):
- Sección 1 (dato/info): 1 + 2 nuevas = 3
- Sección 2 (SI): 1 + 1 nueva = 2
- Sección 3 (arquitectura): 2 base = 2
- Sección 4 (generaciones): 1 base = 1
- Sección 5 (CPU): 5 + 2 nuevas = 7
- Sección 6 (memoria): 3 + 2 nuevas = 5
- Sección 7 (capacidad): 1 base = 1 (+ P6 en 7.1)
- Sección 8 (numeracion): 0 + 2 nuevas = 2
- Sección 9 (caracteres): 1 + 1 nueva = 2

---

*Test v2.0 generado con asistencia de IA — Pendiente validación humana (María / Ana)*
*25 preguntas cubriendo base (15) + contenido ampliado (10)*
*Fecha: 2026-04-23*
