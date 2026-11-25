# Zombie-nvenidos v0.82 — Pisos transitables y accesos a la calle

## Cambios de esta versión

- La colisión del interior del hospital utiliza una **lista cerrada de superficies transitables**: cinco habitaciones a cada lado, pasillo central, recepción, vestíbulo y los diez pasos autorizados. Todo lo demás, incluidos muros y separadores, está prohibido.
- Las puertas de las salas 102–105 y 107–110 tienen un paso físico solo cuando están abiertas. Los accesos a 101 y 106 siguen permanentemente libres.
- La misma comprobación física se aplica a los jugadores y a los zombis. Los zombis de partidas anteriores que aparecían dentro de obstáculos se reubican en suelo válido al entrar.
- Los muros del hospital se vuelven a dibujar en primer plano delante de las siluetas para que los personajes no los tapen visualmente cuando pasan cerca.
- **Las 14 viviendas** tienen accesos dibujados desde la puerta principal y desde el garaje hasta la calzada, incluidas las ocho casas dobles de las parcelas 7, 8, 9 y 11. Los árboles no se generan sobre esos corredores.
- Compatible con supervivencia y creativo, en HTML offline y cliente online PWA.

## Publicación online (Render)

1. Subí los archivos de esta carpeta (no la carpeta que los contiene) al repositorio GitHub conectado a Render.
2. Build Command: `npm install`; Start Command: `npm start`.
3. Después del despliegue, cerrá y reabrí la PWA de ambos dispositivos. Se renovó la clave de caché a v0.82.

## Partidas anteriores

Se conservan los guardados: no se modifica el formato ni la identidad de los hogares. La nueva geometría impide atravesar paredes incluso en partidas anteriores. Como medida preventiva, exportá un guardado antes de actualizar.

## Validaciones realizadas

- Comprobación de sintaxis de JavaScript de ambos clientes y del servidor.
- Prueba en Chromium cargando las versiones online y offline de forma local: inicio, acceso al hospital, puertas cerradas/abiertas, salida y 14 accesos a la calle.
- Exploración de la superficie transitable del hospital: con las ocho puertas cerradas, solo 101 y 106 son accesibles desde el pasillo; con todas abiertas, se puede llegar a las diez salas.
- Prueba del dibujo de los accesos conectados a la calle y verificación de la ausencia de obstáculos en los 28 recorridos inmediatos.

**Pendiente:** prueba de una partida online prolongada en teléfonos reales con distintas condiciones de red; estas pruebas no garantizan ausencia de errores de red o situaciones de carrera aún no observadas.
