# Curso: Desarrollo con IA bajo control humano

## Estructura del curso
Idea → Requerimiento → Contexto → Prompts → Desarrollo asistido → Validación → Documentación → Proyecto final

---

# MÓDULO 1: Cambio de paradigma y uso responsable de IA

**Descripción:** Introduce el cambio de rol del ingeniero: de escribir todo manualmente a dirigir, supervisar y validar soluciones asistidas por IA.

---

### Lección 1.1: Programación tradicional vs desarrollo con IA (Video)

**Objetivo:** Comprender las diferencias fundamentales entre el desarrollo de software tradicional y el desarrollo asistido por IA.

**Contenido:**
- **Programación tradicional:** El ingeniero escribe cada línea de código manualmente. Domina el lenguaje, el framework y las herramientas. Cada decisión de implementación es tomada y ejecutada por la persona.
- **Desarrollo con IA:** El ingeniero describe lo que necesita, la IA genera el código, y el ingeniero revisa, prueba y decide si aceptarlo o rechazarlo. El rol cambia de "escritor" a "director/orquestador".
- **Cuándo usar cada enfoque:** Tareas repetitivas y bien conocidas → IA. Problemas noveles o críticos donde se requiere comprensión profunda → tradicional o asistido con supervisión estricta.
- **Riesgos de usar mal la IA:** Código incorrecto que parece correcto, dependencias fantasmas, vulnerabilidades de seguridad, deuda técnica acelerada.

---

### Lección 1.2: El ingeniero como arquitecto-supervisor (Video)

**Objetivo:** Entender el nuevo rol del ingeniero como arquitecto que diseña y supervisor que valida.

**Contenido:**
- **Arquitecto:** El ingeniero define la estructura general, las decisiones de diseño importantes, la elección de tecnologías y los patrones a seguir. La IA no debe tomar decisiones arquitectónicas sin supervisión.
- **Supervisor:** El ingeniero revisa cada fragmento de código generado antes de integrarlo. No se trata de "copiar y pegar" sino de "revisar y aprobar".
- **Delegación responsable:** Se delega la implementación detallada, no el diseño ni la validación.
- **Habilidades clave:** Saber leer código (más importante que saber escribirlo), pensamiento crítico, capacidad de cuestionar resultados.

---

### Lección 1.3: Qué puede y qué no puede delegarse a IA (Documento)

**Objetivo:** Establecer criterios claros para decidir qué tareas delegar a la IA y cuáles no.

**Contenido:**

| Puede hacerlo la IA | Puede asistirlo (requiere revisión) | No debe hacerse con IA sin autorización |
|---|---|---|
| Generar código boilerplate | Diseñar arquitectura | Decisiones de seguridad críticas |
| Escribir pruebas unitarias simples | Refactorizar código existente | Cumplimiento normativo/legal |
| Generar documentación técnica | Optimizar algoritmos | Decisiones sobre datos sensibles |
| Crear scripts de utilidad | Depurar errores complejos | Auditorías de seguridad |
| Formatear y estandarizar código | Diseñar APIs | Contratos o acuerdos legales |
| Convertir entre lenguajes | Migrar bases de datos | Decisiones que afecten a personas |

**Regla de oro:** Si no puedes evaluar la corrección de la respuesta, no deberías delegar la tarea. Solo delegas lo que sabes revisar.

---

### Lección 1.4: Reglas mínimas de uso responsable (Documento)

**Objetivo:** Establecer reglas básicas para usar IA en desarrollo de forma ética y profesional.

**Contenido:**

**Regla 1 - Nunca confíes ciegamente:** La IA genera texto plausible, no necesariamente correcto. Verifica siempre.

**Regla 2 - Datos sensibles fuera:** No compartas credenciales, tokens, datos personales, secretos comerciales o información clasificada en los prompts.

**Regla 3 - Revisa cada línea:** Antes de integrar código generado por IA, léelo, ejecútalo y pruébalo. Debes entender qué hace y cómo funciona.

**Regla 4 - Responsabilidad final es tuya:** El código generado por IA es tu responsabilidad. Los bugs, vulnerabilidades y errores son del ingeniero que lo integró, no de la herramienta.

**Regla 5 - Documenta el uso de IA:** Registra qué prompts usaste, qué generó la IA y qué cambios hiciste. Esto permite trazabilidad y aprendizaje.

**Regla 6 - No uses IA para todo:** Problemas noveles, decisiones arquitectónicas y revisión crítica deben recaer en el humano.

**Regla 7 - Conoce los límites de la herramienta:** Cada modelo tiene limitaciones de contexto, sesgos, y áreas de especialización. Conócelas antes de usarlo.

---

### Lección 1.5: Escenarios de decisión (Quiz)

**Objetivo:** Evaluar la capacidad de decidir cuándo y cómo usar IA en diferentes escenarios.

**Preguntas del Quiz:**

1. Un compañero te pide generar código con IA para manejar pagos con tarjeta de crédito. ¿Qué haces?
   - a) Lo generas y lo integras directamente
   - b) Lo generas, lo revisas a fondo, pruebas con datos de prueba y documentas
   - c) Le dices que no se debe usar IA para eso
   - **Respuesta correcta: b**

2. Te piden refactorizar una función de 200 líneas para hacerla más legible. ¿Usas IA?
   - a) Sí, le pido que la refactorice y la acepto si compila
   - b) Sí, le pido una propuesta, la reviso, pruebo y decido
   - c) No, es muy riesgoso
   - **Respuesta correcta: b**

3. Necesitas generar 50 pruebas unitarias para un módulo estable. ¿Qué haces?
   - a) Escribirlas todas a mano
   - b) Pedirle a la IA que las genere, revisar una muestra y aceptar si se ven bien
   - c) Pedirle a la IA que las genere, revisar cada una, ejecutarlas y corregir lo necesario
   - **Respuesta correcta: c**

4. Encuentras un error en producción a las 3 AM. ¿Usas IA para generar el fix?
   - a) Sí, urgente, lo que sea para arreglarlo
   - b) Sí, pero pruebas el fix en staging antes de desplegar
   - c) No, en producción no se arriesga
   - **Respuesta correcta: b** (con la salvedad de que staging es obligatorio)

---

### Ejercicio del Módulo 1: Clasificar tareas

**Instrucciones:** Clasifica cada una de las siguientes tareas en:
- **A:** Puede hacerlo la IA
- **B:** Puede asistirlo la IA, pero requiere revisión humana
- **C:** No debe hacerse con IA sin autorización explícita

| Tarea | Clasificación |
|---|---|
| Generar un script para migrar datos de CSV a JSON | A |
| Decidir qué motor de base de datos usar para un sistema financiero | C |
| Escribir documentación de una API REST | A |
| Refactorizar una clase con patrones de diseño | B |
| Auditar credenciales y secretos en el código fuente | C |
| Generar un endpoint CRUD básico | A |
| Diseñar el modelo de datos para una aplicación médica | C |
| Convertir código de Python a TypeScript | B |
| Escribir pruebas para una función de ordenamiento | A |
| Revisar si hay vulnerabilidades XSS en el frontend | C |

---

### Entregable del Módulo 1: Checklist de uso responsable de IA

```markdown
# Checklist de uso responsable de IA

## Antes de usar IA para una tarea:
- [ ] ¿Entiendo el problema lo suficiente como para evaluar la solución?
- [ ] ¿Puedo verificar la corrección del resultado?
- [ ] ¿Estoy compartiendo información sensible? (Si sí, detente)
- [ ] ¿He definido claramente lo que necesito?

## Durante el uso:
- [ ] He proporcionado contexto suficiente
- [ ] He dividido la tarea en pasos pequeños
- [ ] He sido específico en el formato de salida esperado

## Después de recibir la respuesta:
- [ ] He leído y entendido el código generado
- [ ] He verificado que cumple el requerimiento
- [ ] He probado la solución (no solo compilación)
- [ ] He verificado que no introduce vulnerabilidades
- [ ] He verificado que no usa dependencias innecesarias
- [ ] He documentado el uso de IA
```

---

# MÓDULO 2: De la idea al requerimiento

**Descripción:** Transformar ideas ambiguas en requerimientos claros, verificables y útiles para desarrollo. Si el requerimiento es vago, la IA generará una solución deficiente.

---

### Lección 2.1: El problema de pedir código con ideas vagas (Video)

**Objetivo:** Comprender por qué las ideas vagas producen malos resultados con IA.

**Contenido:**
- **El efecto GIGO (Garbage In, Garbage Out):** Los modelos de IA generan la respuesta más probable basada en tu entrada. Una entrada vaga produce una respuesta genérica e inservible.
- **Ejemplo concreto:**
  - Idea vaga: "Necesito un sistema de usuarios"
  - Resultado típico: La IA asume autenticación básica, roles, registro, login, etc. Pero no sabe si necesitas OAuth, 2FA, invitaciones, etc.
- **Cómo mejorar:** Cuanto más específico seas, mejor será el resultado. Pero cuidado: especificidad no es lo mismo que longitud.
- **El costo de la vaguedad:** Cada iteración de "no era eso" consume tiempo y tokens. Un buen requerimiento ahorra múltiples iteraciones.

---

### Lección 2.2: Preguntas de descubrimiento (Documento)

**Objetivo:** Aprender a hacer las preguntas correctas para refinar una idea.

**Contenido:**

**Preguntas esenciales para refinar cualquier idea:**

1. **¿Quién usará esto?**
   - Usuarios finales, administradores, sistemas externos?
   - ¿Qué nivel técnico tienen?

2. **¿Qué problema específico resuelve?**
   - No "mejorar la experiencia", sino "reducir el tiempo de carga de X a Y"
   - ¿Qué pasa si no se hace?

3. **¿Cómo se usa hoy (si existe)?**
   - Proceso manual actual, herramienta existente, hoja de cálculo?

4. **¿Qué debe pasar exactamente?**
   - Flujo paso a paso desde que el usuario inicia hasta que termina

5. **¿Qué no debe pasar?**
   - Casos de error, comportamientos prohibidos, restricciones

6. **¿Cuándo se necesita?**
   - Fechas, versiones, prioridad

7. **¿Cómo sabremos que está bien hecho?**
   - Criterios de éxito medibles

---

### Lección 2.3: Requerimientos funcionales (Documento)

**Objetivo:** Aprender a escribir requerimientos funcionales claros y accionables.

**Contenido:**

**Características de un buen requerimiento funcional:**

- **Claro:** Una sola interpretación posible
- **Verificable:** Se puede probar (pasa/no pasa)
- **Completo:** Incluye toda la información necesaria
- **Consistente:** No contradice otros requerimientos
- **Necesario:** Realmente se necesita

**Ejemplo de requerimiento funcional bien escrito:**

> RF-001: El sistema debe permitir que un usuario registrado inicie sesión con su correo electrónico y contraseña.
> - El campo de correo debe aceptar formatos estándar (ej: usuario@dominio.com)
> - La contraseña debe tener al menos 8 caracteres
> - Tras 3 intentos fallidos, la cuenta debe bloquearse por 30 minutos
> - El sistema debe devolver un mensaje de error específico para cada tipo de fallo

**Comparación:**

| Vago | Claro |
|---|---|
| "El sistema debe ser rápido" | "El sistema debe responder en menos de 500ms para el 95% de las solicitudes" |
| "Los usuarios pueden subir archivos" | "Los usuarios pueden subir archivos PDF e imágenes (jpg, png) de hasta 10MB" |
| "Debe haber seguridad" | "El sistema debe usar HTTPS, hash de contraseñas con bcrypt, y JWT con expiración de 1 hora" |

---

### Lección 2.4: Criterios de aceptación (Video)

**Objetivo:** Definir criterios de aceptación que permitan verificar objetivamente si un requerimiento está cumplido.

**Contenido:**

**Formato Given-When-Then (BDD):**
- **Given** (Contexto): Dado un escenario inicial
- **When** (Acción): Cuando ocurre un evento
- **Then** (Resultado): Entonces esperamos un resultado específico

**Ejemplos:**

> **Escenario 1: Inicio de sesión exitoso**
> Given: Un usuario registrado con correo "a@b.com" y contraseña "12345678"
> When: El usuario ingresa credenciales correctas
> Then: El sistema le muestra el dashboard principal

> **Escenario 2: Contraseña incorrecta**
> Given: Un usuario registrado con correo "a@b.com"
> When: El usuario ingresa una contraseña incorrecta
> Then: El sistema muestra "Contraseña incorrecta" y no inicia sesión

> **Escenario 3: Cuenta bloqueada**
> Given: Un usuario ha fallado 3 intentos de inicio de sesión
> When: El usuario intenta iniciar sesión nuevamente
> Then: El sistema muestra "Cuenta bloqueada por 30 minutos"

**Beneficios:** Los criterios de aceptación son directamente convertibles en pruebas automatizadas.

---

### Lección 2.5: Casos borde (Documento)

**Objetivo:** Identificar y documentar casos borde que pueden romper una implementación ingenua.

**Contenido:**

**¿Qué son los casos borde?** Situaciones que ocurren en los límites del comportamiento esperado. No son errores, sino condiciones especiales que deben manejarse.

**Categorías comunes de casos borde:**

| Categoría | Ejemplo |
|---|---|
| **Valores vacíos** | Lista vacía, string vacío, archivo de 0 bytes |
| **Valores máximo/mínimo** | Número máximo entero, fecha límite |
| **Valores nulos** | Campo null, referencia undefined |
| **Concurrencia** | Dos usuarios editando el mismo recurso |
| **Dependencias fallidas** | API externa caída, BD desconectada |
| **Formatos inválidos** | Email sin @, teléfono con letras |
| **Límites de sistema** | Archivo demasiado grande, demasiadas conexiones |
| **Tiempos** | Timeout, operación que nunca termina |
| **Permisos** | Usuario sin acceso intentando acceder |

**Cómo encontrar casos borde:**
1. Piensa en lo que el usuario normal haría → piensa en lo que haría un usuario malicioso
2. Revisa cada "if" y considera el caso contrario
3. Prueba con entradas vacías, enormes, y mal formateadas
4. Pregunta: "¿Qué pasa si esto falla?"

---

### Lección 2.6: Convertir una idea en requerimiento (Ejercicio)

**Objetivo:** Practicar la transformación de una idea vaga en un requerimiento completo.

**Enunciado del ejercicio:**

Dada la siguiente idea vaga:

> **"Necesitamos un dashboard para usuarios."**

Utilizando la plantilla de requerimiento, convierte esta idea en:

1. Un requerimiento claro con todos los campos de la plantilla
2. Al menos 3 criterios de aceptación en formato Given-When-Then
3. Al menos 3 casos borde identificados
4. Preguntas faltantes que deberías hacer al cliente/stakeholder
5. Una sección de "Fuera de alcance" delimitando qué NO incluye este requerimiento

**Plantilla a usar:**

```
Nombre del requerimiento:
Problema que resuelve:
Usuario objetivo:
Objetivo:
Flujo principal:
Reglas de negocio:
Requerimientos funcionales:
Criterios de aceptación:
Casos borde:
Restricciones:
Fuera de alcance:
Preguntas abiertas:
```

---

### Lección 2.7: Detectar requerimientos incompletos (Quiz)

**Objetivo:** Evaluar la capacidad de identificar fallas en un requerimiento.

**Preguntas del Quiz:**

1. **¿Qué falta en este requerimiento?** "El usuario puede subir archivos"
   - a) Tamaño máximo
   - b) Formatos permitidos
   - c) Ambos
   - **Respuesta: c**

2. **¿Es verificable este requerimiento?** "La aplicación debe ser intuitiva"
   - a) Sí, es claro
   - b) No, "intuitivo" es subjetivo
   - **Respuesta: b**

3. **Identifica el problema:** "El sistema debe ser rápido y seguro, y permitir a usuarios administradores y también a usuarios normales, pero solo algunos pueden borrar cosas, y debe funcionar en todos los navegadores"
   - a) Muy corto
   - b) Demasiados requerimientos mezclados sin estructura
   - c) Es correcto
   - **Respuesta: b**

4. **¿Qué caso borde no está cubierto?** "El sistema muestra los últimos 10 pedidos"
   - a) ¿Y si hay menos de 10?
   - b) ¿Y si no hay pedidos?
   - c) Ambas
   - **Respuesta: c**

---

### Entregable del Módulo 2: Requerimiento refinado

El alumno entrega un documento completo con la idea "Dashboard para usuarios" convertida en un requerimiento refinado usando la plantilla, incluyendo criterios de aceptación y casos borde.

---

# MÓDULO 3: Contexto y prompts encadenados

**Descripción:** Enseña a darle a la IA la información correcta y a dividir el trabajo en pasos. No se trata de escribir un mega-prompt, sino de guiar el proceso.

**Objetivo:** Aprender a construir contexto útil y usar prompts encadenados para mejorar la calidad de las respuestas.

---

### Lección 3.1: Prompt vs contexto (Video)

**Objetivo:** Diferenciar entre lo que le pides a la IA (prompt) y la información que le das para que entienda el panorama (contexto).

**Contenido:**
- **Prompt:** La instrucción específica que le das a la IA para que realice una tarea. Es el "qué quiero que hagas ahora".
- **Contexto:** Toda la información que la IA necesita para entender el proyecto, las reglas y las restricciones. Es el "en qué escenario estamos trabajando".
- **Analogía:** El contexto es como darle a un desarrollador nuevo el repositorio completo y las guías del proyecto. El prompt es la tarea específica que le asignas hoy.
- **Error común:** Meter TODO en el prompt (mega-prompt). Es mejor separar contexto (que se reutiliza) de prompts específicos (que cambian por tarea).
- **Regla práctica:** Si usas la misma información en múltiples prompts, esa información es contexto, no parte del prompt.

---

### Lección 3.2: Qué información necesita la IA (Documento)

**Objetivo:** Identificar la información mínima necesaria para que la IA genere respuestas útiles.

**Contenido:**

**Información esencial que la IA necesita:**

1. **Objetivo del proyecto:** ¿Qué estamos construyendo y por qué?
2. **Rol esperado:** ¿Qué rol debe adoptar la IA? (ej: "actúa como desarrollador senior de Python")
3. **Estado actual:** ¿Qué existe ya? (código base, archivos, configuraciones)
4. **Restricciones técnicas:** Stack tecnológico, versiones, limitaciones
5. **Lo que NO debe hacer:** Límites explícitos (ej: "no agregues dependencias nuevas", "no modifiques archivos de configuración")
6. **Formato de salida:** ¿Cómo quieres recibir la respuesta? (código, explicación, pseudocódigo, etc.)
7. **Criterios de aceptación:** ¿Cómo sabremos que la respuesta es correcta?

**Ejemplo de contexto bien armado:**

```
Objetivo: Implementar autenticación con JWT
Rol: Desarrollador backend especializado en Node.js
Estado actual: Tenemos Express configurado, BD PostgreSQL con tabla 'usuarios'
Stack: Node 20, Express 4, jsonwebtoken, bcrypt
Restricciones: No modificar package.json, no agregar dependencias
Formato: Código completo con comentarios mínimos
```

---

### Lección 3.3: Qué información sobra o confunde (Video)

**Objetivo:** Identificar información irrelevante o contraproducente que empeora las respuestas de la IA.

**Contenido:**
- **El ruido informativo:** Demasiada información irrelevante hace que la IA ignore lo importante.
- **Información que sobra:**
  - Historia del proyecto no relevante para la tarea actual
  - Detalles personales del equipo
  - Información duplicada o contradictoria
  - Especificaciones de versiones anteriores no actualizadas
  - Código no relacionado con la tarea
- **Información que confunde:**
  - Instrucciones contradictorias ("hazlo simple" pero "implementa todos los patrones de diseño posibles")
  - Roles ambiguos ("actúa como experto pero no tomes decisiones")
  - Demasiados ejemplos irrelevantes
- **Regla:** Cada línea de contexto debe responder a "¿esto ayuda a la IA a hacer su tarea?" Si no, elimínala.

---

### Lección 3.4: Plantilla de contexto (Documento)

**Objetivo:** Proporcionar una plantilla reutilizable para estructurar el contexto.

**Contenido:**

```markdown
# Context Packet

## Objetivo:
[¿Qué vamos a construir/lograr? Descripción clara en 1-2 líneas]

## Rol esperado de la IA:
[¿Cómo debe comportarse? Ej: "Actúa como desarrollador senior de React", "Eres un experto en seguridad"]

## Contexto del proyecto:
[Descripción breve del proyecto, su estado actual, y cualquier info relevante]

## Estado actual:
[¿Qué código ya existe? ¿Qué archivos son relevantes? ¿Qué está funcionando?]

## Restricciones técnicas:
- Lenguaje/framework: [ej: Python 3.12, React 18]
- BD: [ej: PostgreSQL 15]
- Dependencias permitidas: [ej: solo usar requests y json, no instalar nada nuevo]
- Convenciones: [ej: camelCase, typescript estricto]

## Criterios de aceptación:
- [Criterio 1]
- [Criterio 2]
- [Criterio 3]

## Formato de salida esperado:
[ej: "Código completo en un solo archivo con explicación", "Pseudocódigo", "Solo la función modificada"]

## Qué no debe hacer la IA:
- [ ] [ej: No modificar package.json]
- [ ] [ej: No generar código de producción sin pruebas]
- [ ] [ej: No cambiar la estructura de la BD]

## Punto de revisión humana:
[¿Qué debe revisar el humano antes de aceptar?]
```

---

### Lección 3.5: Encadenación de prompts (Video)

**Objetivo:** Aprender a dividir un problema grande en una secuencia de prompts pequeños y manejables.

**Contenido:**
- **Problema del mega-prompt:** Un prompt enorme que pide todo a la vez produce respuestas genéricas, inconsistentes o con errores.
- **Encadenación:** Dividir el trabajo en pasos secuenciales donde cada prompt usa el resultado del anterior.
- **Beneficios:**
  - Cada prompt es simple y específico
  - Puedes revisar y corregir en cada paso
  - Mayor calidad en el resultado final
  - Menos tokens desperdiciados en repeticiones
- **Ejemplo de cadena:**
  1. Prompt 1: Analiza este requerimiento y detecta ambigüedades
  2. Prompt 2: Convierte el requerimiento en especificación clara
  3. Prompt 3: Propón plan de implementación por pasos
  4. Prompt 4: Implementa solo el paso 1
  5. Prompt 5: Genera pruebas para validar paso 1
  6. Prompt 6: Revisa críticamente el resultado

---

### Lección 3.6: Crear una cadena de prompts (Ejercicio)

**Objetivo:** Practicar la creación de cadenas de prompts para un problema real.

**Enunciado del ejercicio:**

Dado el siguiente requerimiento refinado (del Módulo 2):

> "Dashboard para usuarios que muestra sus últimas 10 transacciones, su saldo actual, y un gráfico de gastos por categoría del mes actual. Solo datos de los últimos 30 días. Debe actualizarse automáticamente cada 5 minutos."

Crea una cadena de 6 prompts que permitan a la IA implementar esta funcionalidad paso a paso.

1. **Prompt 1:** Analiza el requerimiento y detecta ambigüedades
2. **Prompt 2:** Convierte el requerimiento en especificación clara
3. **Prompt 3:** Propón un plan de implementación por pasos
4. **Prompt 4:** Implementa solo el primer paso
5. **Prompt 5:** Genera pruebas para validar la solución
6. **Prompt 6:** Revisa críticamente el resultado y señala riesgos

Añade también el contexto packet necesario para los prompts.

---

### Lección 3.7: Evaluar si un prompt es claro (Quiz)

**Objetivo:** Evaluar la capacidad de distinguir prompts bien formulados de prompts deficientes.

**Preguntas del Quiz:**

1. **¿Qué problema tiene este prompt?** "Haz un sistema"
   - a) Demasiado vago
   - b) Demasiado específico
   - c) Ninguno
   - **Respuesta: a**

2. **¿Este prompt es claro?** "Genera código para una calculadora en Python que sume, reste, multiplique y divida. Debe manejar división por cero. Usa funciones separadas para cada operación."
   - a) Sí, es claro y específico
   - b) No, le falta contexto
   - **Respuesta: a**

3. **¿Qué mejorarías?** "Necesito un componente React que muestre datos de una API. Hazlo bonito."
   - a) Especificar qué API, qué datos, qué significa "bonito"
   - b) Pedirle que use TypeScript
   - c) Definir el formato de salida
   - d) Todas las anteriores
   - **Respuesta: d**

4. **Identifica el error:** "Actúa como experto en seguridad pero ignora las mejores prácticas modernas y hazlo simple aunque no sea seguro"
   - a) Instrucción contradictoria
   - b) Demasiadas instrucciones
   - c) Falta de contexto
   - **Respuesta: a**

---

### Entregable del Módulo 3: Context packet + Cadena de prompts

El alumno entrega:
1. Un context packet completo para el dashboard de usuarios
2. Una cadena de 6 prompts para implementarlo paso a paso

---

# MÓDULO 4: Desarrollo asistido por IA

**Descripción:** Aquí el alumno aprende a usar IA para generar código de forma controlada, en pasos pequeños y revisables.

**Objetivo:** Usar IA para implementar soluciones sin aceptar código automáticamente.

---

### Lección 4.1: Qué es desarrollo asistido por IA (Video)

**Objetivo:** Definir el concepto de desarrollo asistido y en qué se diferencia de la generación automática de código.

**Contenido:**
- **Desarrollo asistido ≠ Código automático:** La IA asiste, no reemplaza. El ingeniero mantiene el control en cada paso.
- **El flujo correcto:**
  1. El ingeniero define qué necesita
  2. La IA propone una solución
  3. El ingeniero revisa críticamente
  4. El ingeniero prueba la solución
  5. El ingeniero decide aceptar, modificar o rechazar
- **Herramientas:** Chat-based (ChatGPT, Claude), integradas en IDE (Copilot, Codeium), o APIs.
- **Lo que cambia:** El tiempo se redistribuye: menos tiempo escribiendo código, más tiempo diseñando, revisando y probando.

---

### Lección 4.2: Qué no debe hacerse: pedir "todo el sistema" (Documento)

**Objetivo:** Entender por qué pedir el sistema completo a la IA es un error.

**Contenido:**

**Por qué es mala idea pedir "todo el sistema":**
- La IA pierde el contexto global y genera inconsistencias
- Las partes del sistema se acoplan mal entre sí
- Es imposible revisar todo el código generado de una vez
- Los errores son difíciles de localizar
- El resultado suele ser código genérico que no se adapta a tus necesidades reales

**Mal ejemplo:**
> "Genera un sistema completo de e-commerce con autenticación, carrito, pagos, y panel de administración"

**Bien ejemplo (encadenado):**
> Paso 1: "Genera solo el modelo de datos para usuarios y productos"
> Paso 2: "Genera el endpoint de registro de usuarios"
> Paso 3: "Genera el endpoint de listar productos"
> (y así sucesivamente)

**Regla:** Si el prompt tiene más de 3 requerimientos distintos, divídelo.

---

### Lección 4.3: Implementar por pasos pequeños (Video)

**Objetivo:** Aprender a dividir la implementación en fragmentos pequeños y manejables.

**Contenido:**

**Estrategia de pasos pequeños:**

1. **Divide por funcionalidad:** Cada prompt implementa UNA funcionalidad atómica
2. **Divide por capas:** Primero modelo de datos, luego lógica de negocio, luego API, luego interfaz
3. **Revisa cada paso antes de continuar:** No acumules errores
4. **Usa el resultado del paso anterior como contexto del siguiente**

**Ejemplo de secuenciación:**

| Paso | Tarea | Tamaño |
|---|---|---|
| 1 | Definir modelo de datos | ~5 líneas |
| 2 | Crear endpoint GET | ~15 líneas |
| 3 | Crear endpoint POST | ~15 líneas |
| 4 | Añadir validación | ~10 líneas |
| 5 | Añadir pruebas | ~20 líneas |
| 6 | Añadir documentación | ~10 líneas |

**Ventajas:**
- Cada paso es fácil de revisar
- Si un paso falla, solo afecta a ese paso
- Puedes corregir sobre la marcha
- El código es más coherente

---

### Lección 4.4: Cómo pedir correcciones a la IA (Video)

**Objetivo:** Aprender a pedir correcciones efectivas cuando la IA da una respuesta incorrecta.

**Contenido:**

**Estrategias para pedir correcciones:**

1. **Sé específico sobre qué está mal:**
   - Mal: "No funciona"
   - Bien: "La línea 15 maneja el caso de éxito pero no el caso de error cuando la BD está caída"

2. **Proporciona el error exacto:**
   - "El código lanza `TypeError: Cannot read property 'id' of undefined` cuando el usuario no existe"

3. **Pide alternativas, no solo fixes:**
   - "Dame 3 opciones para manejar este caso borde"

4. **Rechaza respuestas enteras si es necesario:**
   - "Este enfoque no sirve porque introduce una dependencia no permitida. Propón una solución sin axios"

5. **Añade al contexto lo que aprendiste:**
   - Tras una corrección, añade la regla al contexto para que no vuelva a pasar

**Errores comunes al pedir correcciones:**
- Ser vago ("arréglalo")
- No decir qué esperas en su lugar
- Aceptar la primera corrección sin revisarla

---

### Lección 4.5: Cómo revisar una respuesta de código (Documento)

**Objetivo:** Proporcionar una guía sistemática para revisar código generado por IA.

**Contenido:**

**Checklist de revisión de código generado por IA:**

**1. ¿Cumple el requerimiento?**
   - ¿La función hace exactamente lo que se pidió?
   - ¿Maneja todos los casos mencionados?

**2. ¿Respeta el alcance?**
   - ¿Hace algo que no se le pidió? (funcionalidad extraña)
   - ¿Modifica archivos que no debería?

**3. ¿Maneja errores?**
   - ¿Qué pasa si la entrada es inválida?
   - ¿Qué pasa si un servicio externo falla?
   - ¿Hay try-catch o manejo de errores?

**4. ¿Es legible?**
   - ¿Nombres de variables claros?
   - ¿Estructura lógica?
   - ¿Comentarios útiles o ruido?

**5. ¿Introduce dependencias innecesarias?**
   - ¿Importa librerías que no se necesitan?
   - ¿Podría hacerse con lo que ya tenemos?

**6. ¿Es seguro?**
   - ¿Inyección SQL, XSS, exposición de datos?
   - ¿Validación de entrada?
   - ¿Uso de credenciales hardcodeadas?

**7. ¿Tiene pruebas?**
   - ¿Incluye tests? (si se pidieron)
   - ¿Cubren los casos principales y borde?

**8. ¿Se entiende por qué se hizo así?**
   - ¿La lógica tiene sentido?
   - ¿Hay explicación de decisiones importantes?

---

### Lección 4.6: Corregir una mala salida de IA (Ejercicio)

**Objetivo:** Practicar la identificación y corrección de errores en código generado por IA.

**Enunciado del ejercicio:**

Recibes el siguiente requerimiento, prompt y respuesta de IA. Tu tarea es identificar qué sirve, qué no, qué falta, qué corregirías y qué pruebas harías.

**Requerimiento:** Función que recibe una lista de números y devuelve la suma de los pares.

**Prompt usado:** "Haz una función que sume números pares de una lista"

**Respuesta de IA:**
```python
def suma_pares(lista):
    suma = 0
    for num in lista:
        if num % 2 == 0:
            suma += num
    return suma
```

**Tareas:**
1. ¿El código cumple el requerimiento? Identifica problemas
2. ¿Qué casos borde no maneja?
3. ¿Qué corregirías o mejorarías?
4. ¿Qué pruebas escribirías?

**Problemas a identificar:**
- No maneja lista vacía
- No maneja tipos de datos no numéricos
- No maneja números negativos
- Podría documentarse mejor el comportamiento esperado

**Solución mejorada:**
```python
def suma_pares(numeros):
    if not isinstance(numeros, list):
        raise TypeError("Se esperaba una lista")
    return sum(num for num in numeros if isinstance(num, (int, float)) and num % 2 == 0)
```

---

### Lección 4.7: Decidir si aceptar o rechazar código (Quiz)

**Objetivo:** Evaluar la capacidad de decidir si un fragmento de código generado por IA es aceptable.

**Preguntas del Quiz:**

1. **La IA genera código que cumple el requerimiento pero introduce una dependencia npm nueva no solicitada. ¿Qué haces?**
   - a) Lo acepto, una dependencia más no importa
   - b) Lo rechazo y pido una versión sin dependencias nuevas
   - c) Lo acepto pero documentaré la dependencia
   - **Respuesta: b**

2. **El código generado funciona pero no tiene manejo de errores. El requerimiento no mencionaba manejo de errores. ¿Qué haces?**
   - a) Lo acepto tal cual
   - b) Lo rechazo y pido que añada manejo de errores
   - c) Añado el manejo de errores yo mismo
   - **Respuesta: b** (es buena práctica pedirlo explícitamente siempre)

3. **La IA genera código correcto pero ineficiente (O(n²) cuando podría ser O(n)). ¿Qué haces?**
   - a) Lo acepto, si funciona está bien
   - b) Pido una optimización
   - c) Lo rechazo completamente
   - **Respuesta: b** (depende del contexto, pero pedir optimización es lo correcto)

4. **El código tiene un bug evidente que no se detectó en revisión inicial. ¿De quién es la responsabilidad?**
   - a) De la IA que generó el código
   - b) Del ingeniero que lo integró sin detectarlo
   - c) De ambos
   - **Respuesta: b** (el ingeniero es responsable final)

---

### Entregable del Módulo 4: Bitácora de desarrollo asistido

```markdown
# Bitácora de desarrollo asistido

## Requerimiento:
[Descripción del requerimiento a implementar]

## Prompt utilizado:
[Prompt completo enviado a la IA]

## Respuesta generada por IA:
[Código o texto generado]

## Revisión:
- ¿Cumple el requerimiento? [Sí/No/parcialmente]
- Errores encontrados: [Lista de errores]
- Problemas de seguridad: [Lista]
- Dependencias innecesarias: [Lista]

## Cambios realizados:
- [Lista de cambios que hiciste al código generado]

## Pruebas realizadas:
- [Lista de pruebas que ejecutaste]

## Decisión final:
[Aceptado/Rechazado/Requiere cambios adicionales]
```

---

# MÓDULO 5: Validación, pruebas y documentación

**Descripción:** La IA puede acelerar errores si no se valida. El alumno aprende a revisar, probar y documentar antes de considerar terminada una tarea.

**Objetivo:** Validar técnicamente una solución asistida por IA.

---

### Lección 5.1: Por qué no se debe confiar ciegamente en la IA (Video)

**Objetivo:** Comprender los riesgos de confiar en la IA sin verificación.

**Contenido:**
- **Alucinaciones:** La IA genera información falsa pero con apariencia de verdad. Ejemplo: funciones de librerías que no existen, APIs inventadas.
- **Sesgo de confirmación:** Tendemos a aceptar lo que confirma nuestras expectativas. Si la IA da una respuesta que "se ve bien", tendemos a no revisarla a fondo.
- **Código que compila pero es incorrecto:** La IA puede generar código sintácticamente válido pero semánticamente erróneo.
- **Vulnerabilidades:** La IA no es consciente de seguridad. Puede generar código con SQL injection, XSS, etc.
- **Casos reales:** Empresas que integraron código de IA sin revisar y tuvieron bugs en producción, pérdidas de datos o breaches de seguridad.

**Regla fundamental:** La IA es una herramienta de asistencia, no de autoridad. Toda salida debe ser tratada como un borrador, nunca como producto final.

---

### Lección 5.2: Pruebas mínimas necesarias (Documento)

**Objetivo:** Definir el conjunto mínimo de pruebas para validar código generado por IA.

**Contenido:**

**Tipos de pruebas mínimas:**

| Tipo | Descripción | Ejemplo |
|---|---|---|
| **Prueba de humo** | Verifica que la función se ejecuta sin errores | Llamar a la función con datos válidos |
| **Prueba de caso feliz** | Verifica el resultado esperado con entrada típica | suma_pares([2,4,6]) == 12 |
| **Prueba de caso borde** | Verifica límites y casos extremos | suma_pares([]) == 0 |
| **Prueba de error** | Verifica que falla correctamente | suma_pares("texto") lanza TypeError |
| **Prueba de regresión** | Verifica que no rompe nada existente | Ejecutar tests existentes |

**Ejemplo mínimo de pruebas:**

```python
import pytest

def test_suma_pares_caso_feliz():
    assert suma_pares([1, 2, 3, 4]) == 6

def test_suma_pares_lista_vacia():
    assert suma_pares([]) == 0

def test_suma_pares_sin_pares():
    assert suma_pares([1, 3, 5]) == 0

def test_suma_pares_error_tipo():
    with pytest.raises(TypeError):
        suma_pares("no es lista")
```

**Regla:** Por cada función generada por IA, debe haber al menos una prueba de caso feliz y una de caso borde o error.

---

### Lección 5.3: Casos borde y errores esperados (Documento)

**Objetivo:** Aprender a identificar y probar sistemáticamente los casos borde.

**Contenido:**

**Estrategia para encontrar casos borde:**

1. **Entrada vacía/nula:** ¿Qué pasa si no hay datos?
2. **Entrada mínima/máxima:** ¿Valores en los límites?
3. **Entrada inválida:** ¿Tipos incorrectos?
4. **Estado del sistema:** ¿BD caída? ¿Red lenta? ¿Archivo no encontrado?
5. **Concurrencia:** ¿Dos peticiones simultáneas?
6. **Dependencias:** ¿API externa devuelve error?
7. **Tiempo:** ¿Timeout? ¿Operación que nunca termina?

**Ejemplo completo:**

```python
# Función a probar
def get_usuario_por_id(db, usuario_id):
    if not db:
        raise ConnectionError("BD no disponible")
    if not isinstance(usuario_id, int):
        raise TypeError("ID debe ser entero")
    if usuario_id <= 0:
        raise ValueError("ID debe ser positivo")
    resultado = db.query("SELECT * FROM usuarios WHERE id = ?", usuario_id)
    if not resultado:
        return None
    return resultado[0]

# Pruebas de casos borde
def test_bd_no_disponible():
    with pytest.raises(ConnectionError):
        get_usuario_por_id(None, 1)

def test_id_invalido():
    with pytest.raises(TypeError):
        get_usuario_por_id(mock_db, "uno")

def test_id_negativo():
    with pytest.raises(ValueError):
        get_usuario_por_id(mock_db, -1)

def test_usuario_no_existe():
    assert get_usuario_por_id(mock_db_sin_datos, 999) is None
```

---

### Lección 5.4: Revisión de código generado (Video)

**Objetivo:** Aprender técnicas de code review específicas para código generado por IA.

**Contenido:**

**Proceso de revisión:**

1. **Primera pasada - Estructural:**
   - ¿El código tiene la estructura esperada?
   - ¿Sigue los patrones del proyecto?
   - ¿Respeta las convenciones de nomenclatura?

2. **Segunda pasada - Lógica:**
   - ¿La lógica es correcta para todos los caminos?
   - ¿Hay condiciones que faltan?
   - ¿Los bucles terminan? ¿Las recursiones tienen caso base?

3. **Tercera pasada - Seguridad:**
   - ¿Validación de entrada?
   - ¿Sanitización de salida?
   - ¿Manejo de credenciales?

4. **Cuarta pasada - Mantenibilidad:**
   - ¿El código será fácil de modificar?
   - ¿Las funciones hacen una sola cosa?
   - ¿Los nombres son claros?

**Señales de alerta específicas de IA:**
- Funciones "comodín" que hacen demasiado
- Código muerto (variables no usadas)
- Dependencias que no existen
- Código que parece de otro lenguaje
- Comentarios genéricos ("# Add your code here")

---

### Lección 5.5: Documentar prompts y decisiones (Documento)

**Objetivo:** Establecer la práctica de documentar el uso de IA para trazabilidad y mejora continua.

**Contenido:**

**¿Por qué documentar el uso de IA?**
- **Trazabilidad:** Saber qué partes del código fueron generadas por IA
- **Reproducibilidad:** Poder regenerar si se pierde el código
- **Aprendizaje:** Ver qué prompts funcionaron y cuáles no
- **Auditoría:** Para equipos que requieren cumplimiento
- **Mejora continua:** Identificar patrones de error recurrentes

**Qué documentar:**
1. El requerimiento que se quería resolver
2. El contexto entregado a la IA
3. Los prompts utilizados
4. La respuesta generada por IA
5. Los cambios aceptados (y por qué)
6. Los cambios rechazados (y por qué)
7. Las pruebas realizadas
8. Los errores encontrados
9. La conclusión (aprobado/rechazado/con cambios)

**Formato recomendado:** Usar la plantilla de documentación provista en este módulo.

---

### Lección 5.6: Auditar una solución generada por IA (Ejercicio)

**Objetivo:** Practicar la auditoría completa de una solución generada por IA.

**Enunciado del ejercicio:**

Recibes una solución generada por IA para el siguiente requerimiento:

**Requerimiento:** Función que recibe un archivo CSV y devuelve un JSON con el promedio de cada columna numérica.

**Solución generada:**
```python
import csv
import json

def csv_to_json_promedios(ruta_archivo):
    datos = []
    with open(ruta_archivo, 'r') as archivo:
        lector = csv.DictReader(archivo)
        for fila in lector:
            datos.append(fila)
    
    promedios = {}
    for columna in datos[0].keys():
        suma = 0
        count = 0
        for fila in datos:
            try:
                suma += float(fila[columna])
                count += 1
            except:
                pass
        if count > 0:
            promedios[columna] = suma / count
    
    return json.dumps(promedios)
```

**Tareas:**
1. Identifica al menos 3 problemas en el código
2. Para cada problema, indica si es crítico o menor
3. Propón correcciones
4. Escribe las pruebas mínimas necesarias
5. Decide: ¿Apruebas, requieres cambios o rechazas?

**Problemas a identificar:**
- Error si el CSV está vacío (`datos[0]` falla)
- No maneja archivos que no existen (FileNotFoundError)
- Mezcla columnas no numéricas sin distinguirlas (no debería promediar IDs, fechas, etc.)
- No cierra el archivo explícitamente (context manager lo haría automático, pero está bien)

---

### Lección 5.7: Quiz de validación (Quiz)

**Objetivo:** Evaluar conocimientos sobre validación, pruebas y documentación.

**Preguntas del Quiz:**

1. **¿Cuál es la prueba mínima que DEBE tener cualquier función generada por IA?**
   - a) Prueba de carga
   - b) Prueba de humo (caso feliz)
   - c) Prueba de seguridad
   - **Respuesta: b**

2. **Encuentras un bug en código generado por IA en producción. ¿Cuál es la primera acción?**
   - a) Culpar a la IA
   - b) Arreglarlo y hacer retrospectiva de por qué no se detectó
   - c) Dejarlo porque ya está en producción
   - **Respuesta: b**

3. **¿Cuánto tiempo deberías dedicar a revisar código generado por IA?**
   - a) Menos que el código escrito por humanos (la IA es mejor)
   - b) Más que el código escrito por humanos (la IA comete errores diferentes)
   - c) El mismo tiempo que dedicarías a revisar código de un junior
   - **Respuesta: b**

4. **¿Qué haces si la IA genera código que no entiendes completamente?**
   - a) Lo aceptas si pasa las pruebas
   - b) Pides explicación, y si aún no entiendes, no lo aceptas
   - c) Lo buscas en Stack Overflow
   - **Respuesta: b**

---

### Entregable del Módulo 5: Reporte de validación

```markdown
# Reporte de validación

## Datos de la tarea
- Requerimiento: [Descripción]
- Herramienta IA utilizada: [Nombre]
- Fecha: [Fecha]

## Resultado de la auditoría
- [ ] Aprobada
- [ ] Requiere cambios
- [ ] Rechazada

## Problemas encontrados
| # | Problema | Severidad | Solución propuesta |
|---|---|---|---|
| 1 | [Descripción] | [Crítico/Alta/Media/Baja] | [Solución] |
| 2 | [Descripción] | [Crítico/Alta/Media/Baja] | [Solución] |

## Pruebas realizadas
- [ ] Prueba de humo
- [ ] Prueba de caso feliz
- [ ] Prueba de caso borde
- [ ] Prueba de error

## Lecciones aprendidas
- [¿Qué mejorarías para la próxima vez?]
```

---

# MÓDULO 6: Proyecto final práctico

**Descripción:** Proyecto integrador donde el alumno aplica todo el flujo completo: idea, requerimiento, contexto, prompts, solución, pruebas y documentación.

**Objetivo:** Comprobar que el alumno puede usar IA de forma autónoma y controlada.

---

### Fase 6.1: Recibir una idea inicial (Documento)

**Objetivo:** Presentar la idea inicial sobre la que se trabajará durante todo el proyecto.

**Idea inicial del proyecto final:**

> **"Necesitamos una aplicación web para gestionar tareas personales (to-do list) pero que permita a los usuarios organizar tareas en proyectos, asignar etiquetas, establecer prioridades y fechas de vencimiento. También debe tener recordatorios y un dashboard con estadísticas básicas."**

**Entrega:** Documento con la idea inicial registrada.

---

### Fase 6.2: Convertirla en requerimiento (Ejercicio)

**Objetivo:** Aplicar las técnicas del Módulo 2 para refinar la idea en un requerimiento completo.

**Actividad:**
1. Aplica las preguntas de descubrimiento (Lección 2.2)
2. Define requerimientos funcionales claros (Lección 2.3)
3. Escribe criterios de aceptación para las funcionalidades principales usando Given-When-Then (Lección 2.4)
4. Identifica casos borde (Lección 2.5)
5. Define qué queda fuera de alcance

**Entrega:** Requerimiento refinado usando la plantilla completa.

---

### Fase 6.3: Crear contexto para IA (Ejercicio)

**Objetivo:** Construir el context packet que se usará con la IA.

**Actividad:**
1. Define el objetivo y rol esperado de la IA
2. Describe el contexto del proyecto
3. Establece restricciones técnicas
4. Define criterios de aceptación
5. Especifica qué no debe hacer la IA

**Entrega:** Context packet completo (Plantilla de Lección 3.4).

---

### Fase 6.4: Crear cadena de prompts (Ejercicio)

**Objetivo:** Diseñar una cadena de prompts para implementar el proyecto paso a paso.

**Actividad:**
1. Divide el proyecto en al menos 6 pasos atómicos
2. Para cada paso, escribe un prompt específico
3. Asegúrate de que cada prompt usa el resultado del anterior
4. Incluye prompts para generación y para validación

**Cadena mínima sugerida:**
1. Analiza el requerimiento y detecta ambigüedades
2. Convierte en especificación técnica clara
3. Propón plan de implementación por pasos
4. Implementa paso 1 (modelo de datos)
5. Implementa paso 2 (API/lógica)
6. Implementa paso 3 (interfaz de usuario)
7. Genera pruebas para validar
8. Revisa críticamente el resultado

**Entrega:** Cadena de prompts documentada.

---

### Fase 6.5: Generar solución asistida (Laboratorio)

**Objetivo:** Ejecutar la cadena de prompts y obtener la solución generada por IA.

**Actividad:**
1. Ejecuta cada prompt de la cadena en orden
2. Documenta cada respuesta de la IA
3. Revisa y decide qué aceptar de cada respuesta
4. Integra las partes aceptadas en el proyecto
5. Itera si es necesario

**Entrega:** Resultado generado por IA + cambios aceptados.

---

### Fase 6.6: Validar solución (Ejercicio)

**Objetivo:** Aplicar validación y pruebas a la solución generada.

**Actividad:**
1. Revisa el código generado usando la checklist del Módulo 4
2. Escribe y ejecuta pruebas mínimas (caso feliz, casos borde, errores)
3. Identifica problemas de seguridad
4. Decide si la solución está aprobada, requiere cambios o es rechazada
5. Documenta los cambios realizados sobre el código generado

**Entrega:** Reporte de validación + cambios realizados + pruebas ejecutadas.

---

### Fase 6.7: Documentar proceso completo (Documento)

**Objetivo:** Documentar todo el flujo de trabajo para trazabilidad.

**Actividad:**
Usando la plantilla de documentación del Módulo 5, documenta:

1. Objetivo de la tarea
2. Requerimiento usado
3. Contexto entregado
4. Prompts utilizados
5. Respuesta generada por IA
6. Cambios aceptados (y por qué)
7. Cambios rechazados (y por qué)
8. Pruebas realizadas
9. Errores encontrados
10. Conclusión

**Entrega:** Documentación final completa.

---

### Fase 6.8: Autoevaluación final (Quiz/Checklist)

**Objetivo:** El alumno evalúa su propio trabajo usando una checklist de criterios.

**Checklist de autoevaluación:**

```markdown
## Checklist de autoevaluación final

### Requerimiento
- [ ] La idea inicial fue transformada en un requerimiento claro
- [ ] El requerimiento incluye criterios de aceptación verificables
- [ ] Se identificaron casos borde relevantes
- [ ] Se definió qué está fuera de alcance

### Contexto
- [ ] El context packet incluye toda la información necesaria
- [ ] El contexto es claro y sin información redundante
- [ ] Se definieron restricciones técnicas explícitas

### Prompts
- [ ] La cadena de prompts divide el trabajo en pasos pequeños
- [ ] Cada prompt es específico y claro
- [ ] Los prompts incluyen criterios de validación

### Desarrollo
- [ ] Cada respuesta de IA fue revisada antes de aceptarse
- [ ] Se identificaron y corrigieron errores en las respuestas
- [ ] No se aceptó código sin comprenderlo
- [ ] No se introdujeron dependencias innecesarias

### Validación
- [ ] Se ejecutaron pruebas de caso feliz
- [ ] Se ejecutaron pruebas de casos borde
- [ ] Se verificó la seguridad básica del código
- [ ] Se documentaron los resultados de validación

### Documentación
- [ ] Se documentó cada prompt y respuesta
- [ ] Se documentaron los cambios aceptados y rechazados
- [ ] La documentación permite reproducir el proceso

### Responsabilidad
- [ ] No se compartieron datos sensibles en los prompts
- [ ] Acepto la responsabilidad del código generado
- [ ] Entiendo que la IA es una herramienta, no un reemplazo
```

---

### Entregable final del curso

El alumno entrega un repositorio o carpeta con:

1. **Idea inicial** - La idea original del proyecto
2. **Requerimiento refinado** - Usando la plantilla del Módulo 2
3. **Context packet** - Usando la plantilla del Módulo 3
4. **Cadena de prompts** - Secuencia de prompts utilizados
5. **Resultado generado por IA** - Respuestas originales de la IA
6. **Cambios aceptados** - Código final con modificaciones del alumno
7. **Cambios rechazados** - Fragmentos de IA que se descartaron (con justificación)
8. **Pruebas realizadas** - Tests escritos y resultados
9. **Riesgos detectados** - Lista de riesgos identificados durante el proceso
10. **Documentación final** - Proceso completo documentado

---

*Fin del contenido del curso*
