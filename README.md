Sistema visual dinámico en p5.js

## Información del proyecto

- **Nombre del proyecto**: Pixel Variable
- **Autor/a**: [Sai Jordán]

## Descripción objetiva

El proyecto es un sistema visual interactivo que genera una cuadrícula de celdas. En cada celda se dibuja aleatoriamente un cuadrado con dos capas concéntricas o un pequeño punto negro. Los colores de los cuadrados cambian según la posición del mouse, y la resolución de la grilla (cantidad de filas y columnas) también es controlada por el mouse. El texto en hexadecimal ("64 65 73 69 67 6E") significa "design" en ASCII y evoca la tipografía Bauhaus.

**Inputs:**  
- Posición horizontal del mouse (`mouseX`) → controla el número de columnas y los tonos de rojo/azul.  
- Posición vertical del mouse (`mouseY`) → controla el número de filas y los tonos de verde.

**Outputs:**  
- Composición visual que se regenera 3 veces por segundo (`frameRate(3)`).  
- Los colores y la densidad de la grilla cambian continuamente al mover el mouse.

## Descripción conceptual

**Idea central:**  
Traducir los principios de la Bauhaus sobre la interacción de tonos y la forma– a un sistema computacional en tiempo real. El usuario modifica la estructura (grilla) y la paleta mediante el movimiento del mouse, generando infinitas variaciones.

**Principio de diseño explorado:**  
La interacción entre el color, la forma y la posición en el espacio (retícula). Se utiliza la aleatoriedad (`random()`) para generar variaciones dentro de reglas fijas, y el mouse como dispositivo de control continuo para que el usuario componga su propia obra.

### Datos que entran, transformación y respuesta visual

| Dato de entrada | Transformación | Respuesta visual |
|----------------|----------------|------------------|
| `mouseX` | `map(mouseX, 0, width, 3, 15)` → número de columnas | La grilla se vuelve más o menos densa horizontalmente |
| `mouseY` | `map(mouseY, 0, height, 4, 20)` → número de filas | La grilla se vuelve más o menos densa verticalmente |
| `mouseX` + `mouseY` | Se convierten en componentes RGB mediante `map` | Los cuadrados cambian de color (tono, saturación) |
| Aleatoriedad (`random()`) | Decide si dibujar cuadrado o punto, y el tamaño interior | Variedad en la composición, evita repetición mecánica |

## Diagrama de flujo

![Diagrama de flujo](diagrama.png)

## Link al sketch en p5.js

Link editable > [https://editor.p5js.org/sai666/sketches/4U2TehZnR](https://editor.p5js.org/sai666/sketches/4U2TehZnR) 
Visualización > [https://editor.p5js.org/sai666/full/4U2TehZnR](https://editor.p5js.org/sai666/full/4U2TehZnR)

