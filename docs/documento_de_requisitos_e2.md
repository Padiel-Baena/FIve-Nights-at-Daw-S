# Especificación de Requisitos y Gestión del Proyecto (E2)

## 1. Tabla de Requisitos

| ID | Descripción | Tipo | Prioridad | Origen |
| :--- | :--- | :--- | :--- | :--- |
| **REQ-01** | El sistema debe permitir iniciar una partida desde el menú principal. | Funcional | Alta | Enunciado |
| **REQ-02** | El sistema debe ejecutar un bucle de microjuegos aleatorios con tiempo límite. | Funcional | Alta | Ten Pages |
| **REQ-03** | El sistema debe llevar un registro de vidas (3 iniciales) y finalizar la partida al agotarse. | Funcional | Alta | Ten Pages |
| **REQ-04** | El sistema debe calcular y acumular la puntuación y racha de aciertos del jugador. | Funcional | Alta | Ten Pages |
| **REQ-05** | El sistema debe incluir 12 microjuegos con mecánicas específicas basadas en ODS. | Funcional | Alta | Ten Pages |
| **REQ-06** | El sistema debe mostrar una pantalla de fin de juego con la puntuación final y opción de reinicio. | Funcional | Media | Ten Pages |
| **REQ-07** | El sistema debe incluir una opción para volver al menú principal en cualquier momento o al finalizar. | Funcional | Media | Enunciado |
| **REQ-08** | El sistema debe permitir consultar la documentación explicativa de los ODS y del juego. | Funcional | Baja | Enunciado |
| **REQ-09** | La interfaz debe ser intuitiva y adaptable a dispositivos móviles y escritorio (*responsive*). | No Funcional | Alta | Enunciado |
| **REQ-10** | Los tiempos de carga entre microjuegos no deben superar los 2 segundos. | No Funcional | Media | Ten Pages |

---

## 2. Historias de Usuario

### HU-01: Iniciar Partida
* **Como:** Jugador
* **Quiero:** Poder pulsar un botón de inicio en el menú principal
* **Para:** Comenzar una sesión de juego inmediatamente
* **Criterios de Aceptación:**
  * CA1.1: El menú principal contiene un botón visible de "Jugar".
  * CA1.2: Al hacer clic en "Jugar", la pantalla cambia a la cuenta atrás/transición del primer microjuego en menos de 1 segundo.

### HU-02: Ejecución de Microjuegos
* **Como:** Jugador
* **Quiero:** Visualizar una instrucción clara de una palabra y un temporizador antes/durante cada microjuego
* **Para:** Saber rápidamente qué acción realizar dentro del tiempo límite
* **Criterios de Aceptación:**
  * CA2.1: Cada microjuego muestra una palabra clave destacada (ej. "¡REPARTE!", "¡APAGA!") durante la transición.
  * CA2.2: Se visualiza una barra de tiempo regressiva en la parte superior que indica el tiempo restante.
  * CA2.3: Si el tiempo llega a 0 sin cumplir el objetivo, la ronda se evalúa como fallo.

### HU-03: Sistema de Puntuación y Vidas
* **Como:** Jugador
* **Quiero:** Ver mis vidas restantes y mi puntuación actual en pantalla
* **Para:** Conocer mi progreso y mantener la tensión del juego
* **Criterios de Aceptación:**
  * CA3.1: El HUD muestra constantemente 3 iconos de vidas y el marcador de puntos.
  * CA3.2: Cada fallo resta 1 vida; al llegar a 0 vidas, se desencadena la pantalla de Game Over.
  * CA3.3: Cada acierto incrementa el marcador y actualiza el contador de racha.

### HU-04: Navegación y Menú
* **Como:** Jugador
* **Quiero:** Volver al menú principal desde la pantalla de fin de juego o pausar la partida
* **Para:** Reiniciar el juego o cambiar de actividad
* **Criterios de Aceptación:**
  * CA4.1: La pantalla de Game Over ofrece los botones "Reintentar" y "Menú Principal".
  * CA4.2: Al seleccionar "Menú Principal", se restablece el estado del juego (puntos a 0, vidas a 3).

### HU-05: Consulta de Documentación
* **Como:** Jugador / Educador
* **Quiero:** Acceder a una sección de información sobre los ODS
* **Para:** Comprender el trasfondo educativo de cada microjuego
* **Criterios de Aceptación:**
  * CA5.1: El menú principal incluye un botón "Instrucciones / ODS".
  * CA5.2: Al pulsarlo, se despliega una vista modal o página secundaria con el resumen de los ODS trabajados.

---

## 3. Diagrama de Casos de Uso

```
                        +-----------------------------------+
                        |         EcoRush: Desafío ODS      |
                        |                                   |
                        |  ( Iniciar Partida )              |
                        |           ^                       |
                        |           | <<include>>           |
                        |           v                       |
     +---------+        |  ( Jugar Microjuego )             |
     |         |------->|                                   |
     | Jugador |------->|  ( Consultar Puntuación )         |
     |         |------->|                                   |
     +---------+        |  ( Volver al Menú )               |
                        |                                   |
                        |  ( Consultar Documentación / ODS )|
                        +-----------------------------------+
```

---

## 4. Tarjetas del Backlog y Enlaces

| ID Tarjeta | Título de la Tarjeta | Enlace / Ubicación en Tablero |
| :--- | :--- | :--- |
| **CARD-01** | Configuración de Pantalla de Menú Principal | `[Tablero Kanban / Columna ToDo / #1]` |
| **CARD-02** | Motor de Game Loop y Gestión de Estados | `[Tablero Kanban / Columna ToDo / #2]` |
| **CARD-03** | Sistema de HUD (Vidas, Puntos y Temporizador) | `[Tablero Kanban / Columna ToDo / #3]` |
| **CARD-04** | Desarrollo de Microjuegos de Tipo Clic (Luces, Grifo, Incendio) | `[Tablero Kanban / Columna ToDo / #4]` |
| **CARD-05** | Desarrollo de Microjuegos Drag & Drop (Basura, Equipar) | `[Tablero Kanban / Columna ToDo / #5]` |
| **CARD-06** | Desarrollo de Microjuegos de Elección (Vaso, Preguntas, Planta/Destruye) | `[Tablero Kanban / Columna ToDo / #6]` |
| **CARD-07** | Desarrollo de Microjuegos de Esquivar / Movimiento (Pez, Pato, Cinta) | `[Tablero Kanban / Columna ToDo / #7]` |
| **CARD-08** | Pantalla de Fin de Juego y Resumen ODS | `[Tablero Kanban / Columna ToDo / #8]` |
| **CARD-09** | Vista de Documentación e Instrucciones ODS | `[Tablero Kanban / Columna ToDo / #9]` |

---

## 5. Registro de Decisiones sobre Ambigüedades

1. **Ambigüedad en el Microjuego "Planta o Destruye":**
   * *Pregunta:* ¿Cómo balancear la acción de talar sin promover la deforestación?
   * *Decisión:* Solo se permite talar árboles enfermos o secos. Talar un árbol sano penaliza con pérdida de punto/vida.

2. **Mecánica de Controles en Dispositivos Móviles:**
   * *Pregunta:* ¿Cómo adaptar el juego "Salva al Pez" que originalmente plantea teclas `[←]` `[→]`?
   * *Decisión:* Se implementará un control dual: teclas de flecha en teclado y zonas de toque/arrastre lateral en pantallas táctiles.

3. **Duración de los Microjuegos:**
   * *Pregunta:* Algunos microjuegos planteaban tiempos dispares (3 a 60 segundos).
   * *Decisión:* Para mantener el ritmo estilo *WarioWare*, todos los microjuegos se ajustarán a un rango de entre 3 y 10 segundos según su nivel de dificultad.

---

## 6. Matriz de Trazabilidad Inicial

| Requisito | Historia de Usuario | Tarjeta del Backlog | Criterio de Aceptación Comprobable |
| :--- | :--- | :--- | :--- |
| **REQ-01** | HU-01 (Iniciar Partida) | CARD-01 | CA1.1, CA1.2 |
| **REQ-02** | HU-02 (Ejecución de Microjuegos) | CARD-02 | CA2.1, CA2.2 |
| **REQ-03** | HU-03 (Sistema de Puntuación y Vidas) | CARD-03 | CA3.1, CA3.2 |
| **REQ-04** | HU-03 (Sistema de Puntuación y Vidas) | CARD-03 | CA3.3 |
| **REQ-05** | HU-02 (Ejecución de Microjuegos) | CARD-04, CARD-05, CARD-06, CARD-07 | CA2.1, CA2.3 |
| **REQ-06** | HU-04 (Navegación y Menú) | CARD-08 | CA4.1 |
| **REQ-07** | HU-04 (Navegación y Menú) | CARD-01, CARD-08 | CA4.2 |
| **REQ-08** | HU-05 (Consulta de Documentación) | CARD-09 | CA5.1, CA5.2 |
| **REQ-09** | HU-01, HU-02 | CARD-01, CARD-02 | Verificación visual en pantallas < 768px y > 1024px |
| **REQ-10** | HU-02 | CARD-02 | Medición de latencia de cambio entre microjuegos (< 2000 ms) |
