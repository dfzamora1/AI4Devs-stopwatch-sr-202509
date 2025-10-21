# prompts.md – AI4Devs Stopwatch/Countdown

## 0) Prompt REAL escrito por mí (inicio de la sesión)
> **"Hola. Me ayudas por favor a revisar qué debo hacer leyendo este link de GitHub: https://github.com/LIDR-academy/AI4Devs-stopwatch-sr-202509"**

Este fue el punto de partida. A partir de ahí, el asistente resumió los requisitos del repositorio y propuso un plan.

## 1) Objetivo interpretado (del repositorio)
- Construir un **cronómetro** y una **cuenta regresiva** en `index.html` + `script.js` usando el template del repo.
- Permitir **múltiples instancias** (varios cronómetros/contadores).
- Al finalizar la cuenta regresiva: **enviar notificación** y **reproducir un sonido**.
- Entregar por **Pull Request** en una carpeta `stopwatch-<iniciales>` + `prompts.md` + `chatbot.md` y pegar el **prompt final** en el comentario del PR.

## 2) Iteraciones de la conversación (lo que pedí/alimenté al chatbot)
- Confirmé: **“sI”** (solicité que me generaran los archivos base para pegar).
- Luego pedí: **“SI”** (generar `prompts.md` y `chatbot.md`).

> Nota: Aunque mis mensajes fueron breves (“sI/ SI”), el asistente convirtió esto en instrucciones operativas para construir el código. Por eso, documento abajo el **prompt operativo** que se usó para generar los archivos, a efectos de trazabilidad del reto.

## 3) Prompt operativo (usado para construir los archivos)
> Genera `index.html` y `script.js` para un app web que maneje **múltiples** cronómetros y cuentas regresivas. Cada tarjeta debe mostrar tiempo en formato `hh:mm:ss.cc` (ocultar hh si 0). Cronómetro: iniciar/pausar/reiniciar. Cuenta regresiva: inputs h/m/s con validaciones; al llegar a 0, notificar al usuario mediante la **Notification API** (tras conceder permisos) y reproducir un beep con **WebAudio API**. Implementa clases `Stopwatch` y `Countdown`, usa `requestAnimationFrame` y `performance.now()` para el tick. Añade dos botones globales: “Activar notificaciones” y “Probar sonido”. Estilos sencillos responsive sin frameworks. Nombres de archivo exactos: `index.html` y `script.js`.

### Por qué este prompt operativo
Traduce los requisitos del repo en especificaciones técnicas precisas (clases, APIs, formato tiempo, multi‑instancia, permisos/UX).

## 4) Prompt FINAL para pegar en el comentario del PR
> Construí la solución basada en: **cronómetro + cuenta regresiva con múltiples instancias**, notificación del navegador y beep al finalizar, clases `Stopwatch`/`Countdown` con `requestAnimationFrame` + `performance.now()`, botones globales para activar notificaciones y probar audio, y archivos **`index.html`** + **`script.js`**. El diseño es responsivo sencillo sin frameworks. Este fue el prompt operativo usado para generar el código.

## 5) Lecciones / ajustes
- **Nombre de archivo**: `script.js` (sin “s”).
- **Notificaciones**: requieren permiso; se añadió botón para solicitarlas.
- **Audio**: algunos navegadores bloquean autoplay; botón “Probar sonido” desbloquea el contexto.
- **Precisión**: se evita `setInterval` en favor de `requestAnimationFrame` + delta de tiempo.
