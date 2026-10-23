# Memorama Vikings Corp.

Juego de memorama con estilo de casino para la activación de marca de **Vikings Corp.**, cadena de gimnasios en Monterrey. Está pensado para una pantalla táctil de 50" y para tablet.

## Características
- PWA en HTML, CSS y JS puro, sin dependencias ni build.
- Funciona sin internet una vez instalada (service worker).
- Responsive: el tablero se acomoda solo en horizontal y en vertical.
- Teclado en pantalla para capturar el nombre del jugador.
- Tabla de campeones que vive solo en memoria y se borra al recargar.
- Sonidos generados con Web Audio API (no usa archivos de audio).
- Animaciones de casino: volteo 3D, chispas, focos de marquesina, contador tipo tragamonedas y lluvia de fichas.

## Configuración
Al inicio del script en `index.html`, en el objeto `CONFIG`:

| Opción | Qué hace |
|---|---|
| `pares` | Cuántos pares salen (de 4 a 12) |
| `tiempo` | Segundos por partida |
| `puntosPorPar` | Puntos por cada par encontrado |
| `puntosPorSegundo` | Puntos por segundo sobrante al completar |
| `regresarInicioSeg` | Segundos en resultados antes de volver al inicio |

Las imágenes se toman en el orden de la lista `ORDEN`.

## Publicar
Despliega la carpeta tal cual en Vercel (o cualquier hosting estático). En cada dispositivo, abre el sitio una vez con internet, instálalo como app y pruébalo en modo avión.

Cada vez que actualices archivos, sube la versión de `CACHE` en `sw.js` (por ejemplo `v6` → `v7`) para que los dispositivos descarguen lo nuevo.

## Probar en local
Abre `index.html` con doble clic. El juego funciona completo; el modo sin conexión solo se activa servido por http(s).
