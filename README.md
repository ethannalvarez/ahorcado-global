# Ahorcado Global

Juego del ahorcado hecho con JavaScript en el que se adivinan **continentes, países, océanos y maravillas naturales**. Es un proyecto personal que desarrollo en mi tiempo libre y que sigo mejorando.

**Jugar:** https://ethannalvarez.github.io/ahorcado-global/

## Estado actual

Versión básica y funcional:

- Tablero del ahorcado, casillas de la palabra y teclado en pantalla, con tema oscuro.
- Conjunto limitado de palabras. Empecé con un par de palabras para centrarme en manejar los eventos del juego.
- Detección de victoria y derrota corregida tras detectar varios fallos.
- Una misma palabra no se repite en los 5 intentos siguientes.

## Cómo funciona

El juego sigue un patrón clásico: **estado en memoria y manipulación directa del DOM**. Toda la información de la partida vive en tres variables de JavaScript. Cada vez que se pulsa una letra, la función `handleGuess()` las actualiza y sincroniza los elementos HTML afectados.

| Variable | Qué guarda |
|---|---|
| `selectedWord` | La palabra secreta, elegida al azar al iniciar la partida con `initGame()`. |
| `guessedLetters` | Las letras ya probadas, en un `Set` para evitar duplicados y comprobar al instante con `.has(letter)`. |
| `mistakes` | Contador de fallos acumulados. |

Para evitar repeticiones uso una **cola FIFO (First In, First Out) de tamaño 5** que actúa como historial de palabras bloqueadas.

## Qué he aprendido

- A manejar eventos en JavaScript.
- La lógica del ahorcado y la detección de victoria o derrota.
- A evitar problemas como que se repita la misma palabra en los 5 intentos siguientes.

## Próximas mejoras

- [ ] Renovar el diseño y la estética del juego.
- [ ] Interactividad al ganar o fallar: animaciones de victoria y efectos de interfaz para hacerlo más atractivo.
- [ ] Ampliar el diccionario de palabras y organizarlo en categorías.
- [ ] Cambiar la cola FIFO por un patrón de baraja (Deck), para que ninguna palabra se repita hasta haberlas jugado todas.

## Cómo ejecutarlo en local

Descarga el repositorio y abre `index.html` en el navegador. No necesita instalar nada.

## Autor

Ethan Álvarez Rodríguez, estudiante de Ingeniería de Telecomunicaciones (Telemática) en la Universidad de Vigo.

- GitHub: [@ethannalvarez](https://github.com/ethannalvarez)
- LinkedIn: [Ethan Álvarez Rodríguez](https://www.linkedin.com/in/ethan-%C3%A1lvarez-rodr%C3%ADguez)
