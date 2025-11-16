Circuito digital desarrollado en Logisim que implementa un juego basado en una matriz 6×6 de bloques, donde cada celda posee un estado fijo: Suelo de hielo, Suelo de goma, Pozo o Premio. El jugador inicia en la posición (0,0) y debe desplazarse entre celdas adyacentes siguiendo las reglas definidas. El objetivo es llegar a la última columna sin caer en un Pozo; en caso contrario, la partida finaliza como perdida.

El sistema muestra en todo momento la posición actual del jugador, su identificador y el estado del bloque correspondiente. Maneja hasta 4 jugadores y mantiene el historial de sus partidas mientras la simulación esté activa. Al finalizar cada juego, informa si fue ganado o perdido y calcula el puntaje según los premios obtenidos o el Pozo encontrado.

## Reglas principales del juego

- El jugador se mueve una celda por vez hacia arriba, abajo, izquierda o derecha.
- Si pisa Suelo de hielo, patina automáticamente dos posiciones en la misma dirección.
- Si toca un Pozo, la partida termina inmediatamente con puntaje –1.
- Si llega a la columna final y la celda no es Pozo, gana sumando 5 puntos por cada Premio atravesado.
- Los movimientos inválidos (bordes de la matriz) no alteran la posición.

## Sobre la implementación

El diseño utiliza:

- Sistemas combinacionales para determinar el estado de cada celda y las reglas de movimiento.
- Sistemas secuenciales (flip-flops y registros) para almacenar posición, transiciones, historial y avance del juego.
- Control por reloj, permitiendo movimientos sincronizados y estados intermedios correctos.
- Módulos estructurados para cada parte del circuito, facilitando entender qué componente aplica cada regla del juego.

- <img width="919" height="514" alt="image" src="https://github.com/user-attachments/assets/f45ac555-4dd4-4cbb-9681-cbf44316bdd8" />
