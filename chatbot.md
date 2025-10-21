# chatbot.md – Experiencia usando el/los chatbots

## Herramienta utilizada
- ChatGPT (modelo GPT‑5 Thinking). Español.

## Qué pedí exactamente
- Revisar el repositorio y decirme qué debía hacer.
- Luego pedí que generara un esqueleto funcional (`index.html` + `script.js`).
- Después solicité las plantillas `prompts.md` y `chatbot.md`.

## Flujo de trabajo
1. **Lectura del repo** → Lista de requisitos.
2. **Diseño** → Clases `Stopwatch` y `Countdown`, utilidades (`fmt`, `beep`, notificaciones), layout de tarjetas.
3. **Entrega** → Archivos listos para pegar + documentación.
4. **Ajuste** → Alinear `prompts.md` con mi **prompt real** de inicio y la evolución de la conversación.

## Problemas / decisiones
- **Permisos de notificación** y **audio autoplay** → botones dedicados.
- **Precisión** → `requestAnimationFrame` y `performance.now()`.
- **Multiplicidad** → cada tarjeta mantiene su propio estado.

## Próximos pasos posibles
- Persistir estado con `localStorage`.
- Laps en el cronómetro y sonidos configurables.
- Tests E2E del flujo countdown → 0 → notificación.

## Evaluación
La solución cumple los requisitos (cronómetro, cuenta regresiva, múltiples instancias, notificación y sonido), sin dependencias externas y con UX mínima.
