# Tema 11 — Caso Práctico

> **Título**: Informática básica. Representación y comunicación de la información.
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid
> **Estado**: PILOTO v1.0 — Pendiente validación
> **Tiempo estimado**: 30 minutos

---

## Enunciado

El Ayuntamiento de Madrid está renovando los equipos informáticos del área de Atención al Ciudadano. Como técnico auxiliar TIC, se le asigna la tarea de evaluar las especificaciones técnicas de los nuevos equipos propuestos y asesorar sobre su adecuación.

El proveedor ha presentado la siguiente propuesta para 50 puestos de trabajo:

| Componente | Especificación |
|---|---|
| Procesador | Intel Core i5-13400 (arquitectura x86, 10 núcleos, 16 hilos) |
| Memoria RAM | 16 GB DDR4-3200 (2 x 8 GB) |
| Almacenamiento | SSD NVMe 512 GB |
| Firmware | UEFI con Secure Boot habilitado |
| Sistema Operativo | Windows 11 Pro |

---

## Cuestiones

### Cuestión 1 — Arquitectura del procesador (2 puntos)

a) Indique a que tipo de arquitectura de conjunto de instrucciones pertenece el procesador Intel Core i5-13400 (CISC o RISC). Justifique su respuesta.

b) Explique brevemente cómo es posible que un procesador de este tipo consiga un rendimiento elevado a pesar de utilizar instrucciones complejas.

<details>
<summary>Respuesta orientativa</summary>

a) El Intel Core i5-13400 pertenece a la arquitectura **CISC** (Complex Instruction Set Computer), ya que forma parte de la familia x86 de Intel. Los procesadores CISC se caracterizan por disponer de un conjunto amplio de instrucciones complejas que permiten operaciones entre operandos en memoria y registros.

b) A pesar de ser CISC, los procesadores x86 modernos alcanzan alto rendimiento porque internamente **traducen las instrucciones complejas CISC a microinstrucciones simples tipo RISC** antes de ejecutarlas. De esta forma combinan la compatibilidad del set de instrucciones x86 con la eficiencia de ejecución de las arquitecturas RISC.

*Referencia: tema-11-contenido.md, sección 5.2.1*
</details>

---

### Cuestión 2 — MultiThreading (2 puntos)

El procesador especificado tiene 10 núcleos y 16 hilos.

a) Explique que tecnología permite que un procesador tenga mas hilos que núcleos físicos y como la denomina Intel.

b) Si 6 de los 10 núcleos soportan esta tecnología y los 4 restantes no, justifique matemáticamente los 16 hilos totales.

<details>
<summary>Respuesta orientativa</summary>

a) La tecnología se denomina **HyperThreading** (nombre comercial de Intel) o **MultiThreading**. Permite duplicar las unidades lógicas de cada núcleo, de modo que un único núcleo físico puede ejecutar dos tareas (hilos) de forma simultánea. AMD denomina a su implementación equivalente **SMT (Simultaneous Multi-Threading)**.

b) Cálculo:
- 6 núcleos con HyperThreading: 6 x 2 = 12 hilos
- 4 núcleos sin HyperThreading: 4 x 1 = 4 hilos
- **Total: 12 + 4 = 16 hilos**

Esto corresponde a la arquitectura híbrida de Intel (P-cores con HT + E-cores sin HT).

*Referencia: tema-11-contenido.md, sección 5.2.3*
</details>

---

### Cuestión 3 — Memoria RAM (3 puntos)

La propuesta incluye 16 GB DDR4-3200 en configuración 2 x 8 GB.

a) Indique cuántos pines tienen los módulos DDR4 y en que rango de frecuencias operan según la especificación estándar.

b) Explique que es la tecnología Dual Channel y que requisitos deben cumplir los módulos para activarla. Indique si la configuración propuesta (2 x 8 GB) cumple estos requisitos.

c) Si el área de Atención al Ciudadano trabaja con aplicaciones críticas que no admiten errores en memoria, recomendaría RAM ECC o No-ECC? Justifique su respuesta indicando las implicaciones.

<details>
<summary>Respuesta orientativa</summary>

a) Los módulos DDR4 tienen **288 pines** y operan en un rango de frecuencia estándar de **2133 a 4000 MHz**. DDR4-3200 indica una frecuencia de 3200 MHz, dentro del rango estándar.

b) **Dual Channel** permite a la CPU trabajar con dos canales independientes y simultáneos para acceder a datos, **duplicando el ancho de banda**. Requisitos: los 2 módulos deben tener la **misma frecuencia, misma capacidad y misma latencia**. La configuración 2 x 8 GB cumple los requisitos si ambos módulos son idénticos en frecuencia (3200 MHz), capacidad (8 GB) y latencia (CL).

c) Para aplicaciones críticas de Atención al Ciudadano, la elección depende del contexto:
- **RAM ECC** detecta y corrige errores de 1 bit mediante un sistema de paridad. Se usa en servidores y entornos críticos. Requiere que placa base y procesador soporten ECC.
- **RAM No-ECC** no tiene corrección de errores. Es la habitual en PCs de escritorio.

Para puestos de atención al ciudadano (no servidores), la recomendación sería **No-ECC**, ya que el Intel i5-13400 no soporta ECC y los errores de memoria en puestos de trabajo individuales no suponen un riesgo crítico. La fiabilidad crítica debe garantizarse a nivel de **servidor** (donde si debería usarse ECC).

*Referencia: tema-11-contenido.md, secciones 6.2.2, 6.2.4, 6.2.6*
</details>

---

### Cuestión 4 — BIOS vs UEFI (2 puntos)

a) Indique tres diferencias entre BIOS y UEFI que sean relevantes para la seguridad y el rendimiento de los equipos del Ayuntamiento.

b) Explique que es Secure Boot y por qué es relevante en un entorno de administración pública.

<details>
<summary>Respuesta orientativa</summary>

a) Tres diferencias relevantes:

| Aspecto | BIOS | UEFI |
|---|---|---|
| **Arranque** | Más lento | Más rápido (mejor productividad) |
| **Seguridad** | Sin arranque seguro | Secure Boot protege contra bootkits |
| **Particiones** | 4 particiones MBR, max 2,2 TB | 128 particiones GPT, max 8 ZB (permite discos grandes) |

b) **Secure Boot** es una funcionalidad de UEFI que verifica que el sistema operativo que se va a cargar esta **autenticado digitalmente** antes de permitir su ejecución. Evita el inicio de software no autorizado (bootkits, rootkits) que podría ejecutarse antes del sistema operativo.

En un entorno de administración pública es relevante porque:
- Protege contra malware que se ejecuta antes de que el antivirus este activo.
- Cumple con los requisitos del **Esquema Nacional de Seguridad** en cuánto a integridad del arranque.
- Impide la manipulacion del sistema de arranque por usuarios no autorizados.

*Referencia: tema-11-contenido.md, sección 6.4 [UEFI-SPEC]*
</details>

---

### Cuestión 5 — Codificación de caracteres (1 punto)

Los formularios de Atención al Ciudadano deben admitir nombres con caracteres especiales (acentos, ene, cedilla) y eventualmente caracteres de otros alfabetos (cirílico, árabe).

Que codificación de caracteres recomendaría para la base de datos que almacene estos datos? Justifique su respuesta.

<details>
<summary>Respuesta orientativa</summary>

Se recomienda **UTF-8** por las siguientes razones:

1. **Universalidad**: permite representar cualquier carácter del estándar Unicode, incluyendo latin con diacriticos (acentos, ene, cedilla), cirílico, árabe y cualquier otro alfabeto.
2. **Compatibilidad**: es compatible con US-ASCII, por lo que los caracteres básicos ocupan solo 1 byte (eficiencia en textos predominantemente latinos).
3. **Estándar web**: es la codificación dominante en la web y recomendada por el W3C, facilitando la interoperabilidad con otros sistemas.
4. **Autosincronización**: evita ambigüedades en la decodificación de caracteres multibyte.

Alternativas descartadas:
- ISO-8859-1/Latin-1: solo cubre Europa occidental, no soporta cirílico ni árabe.
- EBCDIC: propietario de IBM, no estándar.
- UTF-16: menos eficiente para textos predominantemente latinos (2 bytes mínimo vs 1 en UTF-8).

*Referencia: tema-11-contenido.md, sección 9.3 [UNICODE-STD]*
</details>

---

## Criterios de evaluación

| Cuestión | Puntos | Evaluación |
|---|---|---|
| 1. Arquitectura CISC/RISC | 2 | Identificación correcta + justificacion microinstrucciones |
| 2. MultiThreading | 2 | Concepto HT/SMT + cálculo correcto 16 hilos |
| 3. Memoria RAM | 3 | Pines DDR4 + Dual Channel + ECC justificado |
| 4. BIOS/UEFI | 2 | 3 diferencias + Secure Boot + contexto AAPP |
| 5. Codificación | 1 | UTF-8 + justificacion completa |
| **Total** | **10** | |

---

*Caso práctico generado con asistencia de IA — Pendiente validación humana*
*Contexto: supuesto práctico de nivel C1 TIC para Ayuntamiento de Madrid*
*Fecha: 2026-04-16*
