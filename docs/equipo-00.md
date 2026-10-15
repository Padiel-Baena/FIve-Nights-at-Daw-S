# Ian Borja Tomas | Supervisor de Producto |Ian-Ian-Ian-Ian-Ian

# Pablo Daniel Baena | Supervisor QA | Padiel-Baena

# Diego Plana| Facilitación | Diego Plana

# Carlos Garrido Romero | Supervisor de Arquitectura, Supervisor Integración |Carlos240726

---

# Normas de trabajo en equipo

## 1. Canal de comunicación

Utilizaremos un grupo de Discord para comunicarnos, resolver dudas y avisar de problemas. Los cambios de código y las tareas se gestionarán mediante GitHub.

## 2. Plazo máximo para revisar un PR

Cada Pull Request (PR) deberá revisarse en un plazo máximo de **24 horas**. Si se solicitan cambios, el autor deberá corregirlos lo antes posible.

## 3. Incumplimiento de las normas

## Si alguien no cumple los plazos o las responsabilidades asignadas, se le avisará para que pueda solucionarlo. Si el incumplimiento se repite, el equipo hablará con esa persona para acordar una solución y redistribuir las tareas si es necesario.

# Convenciones de desarrollo

## 1. Nombres de las ramas

Las ramas seguirán el formato `features/[nombre-minijuego]` o `features/[nombre-tarea]`, utilizando nombres descriptivos relacionados con el minijuego o la funcionalidad que se esté desarrollando.

**Ejemplos:**

- `features/minijuego-memoria`
- `features/minijuego-reflejos`
- `features/sistema-puntuacion`
- `features/pantalla-menu`

## 2. Mensajes de commit

Los mensajes de commit seguirán la estructura **verbo + qué cambia**, describiendo brevemente el cambio realizado.

**Ejemplos:**

- `Añadir minijuego de memoria`
- `Corregir detección de clics en el minijuego`
- `Actualizar sistema de puntuación`
- `Mejorar transición entre minijuegos`
- `Eliminar errores en el contador de tiempo`

## 3. Idioma del código y de los comentarios

El código, los comentarios y los nombres de variables, métodos y clases se escribirán en **inglés** para mantener la coherencia en todo el proyecto.

Se utilizarán las siguientes convenciones de nombres:

- **Clases:** `PascalCase` (ejemplo: `MemoryMinigame`).
- **Métodos y variables:** `camelCase` (ejemplo: `startMinigame`).
- **Constantes:** `UPPER_SNAKE_CASE` (ejemplo: `MAX_ROUND_TIME`).
- **Archivos:** utilizarán nombres descriptivos relacionados con su funcionalidad (ejemplo: `MemoryMinigame.java`).

---

# Definición de hecho (Definition of Done)

Una tarjeta solo podrá pasar al estado **Done** cuando cumpla todos los siguientes requisitos:

- [ ] El Pull Request (PR) ha sido revisado y aprobado por otra persona del equipo.
- [ ] Los cambios se han fusionado correctamente en la rama `main`.
- [ ] La documentación afectada se ha actualizado, si es necesario.
- [ ] El minijuego o la funcionalidad funciona correctamente y cumple los requisitos establecidos.
