<!-- l10n-sync: source-file="workshop/00-overview.md" -->
# 🎮 Mona Mayhem — Taller de GitHub Copilot

---

> **Duración:** ~1 hora  
> **Nivel:** Intermedio  
> **Stack:** Astro / Node.js / TypeScript

Crea una aplicación retro estilo arcade para comparar contribuciones de GitHub — **Mona Mayhem** — mientras aprendes el espectro completo de flujos de trabajo de GitHub Copilot. El taller admite **dos rutas**: una experiencia de VS Code y otra de GitHub Copilot CLI.

---

## 🎯 Elige tu ruta

- **Ruta de VS Code** — quédate dentro del editor y practica Chat, Plan Mode, Agent Mode, agentes en segundo plano y el ciclo de revisión integrado.
- **Ruta de CLI** — quédate en la terminal y practica `copilot`, contexto con `@file`, `/plan`, ediciones automáticas, `/fleet`, `/delegate` y `/review`.

Sigue la ruta que mejor se adapte a tu flujo de trabajo.

---

## 📋 Lista rápida de comprobación

Antes de empezar, comprueba:

- [ ] GitHub Copilot está habilitado para tu cuenta
- [ ] Node.js instalado
- [ ] Git instalado y configurado
- [ ] Tu navegador y terminal están listos

<!-- track:vscode:start -->
- [ ] VS Code **v1.107+** (sin actualizaciones pendientes)
- [ ] Iniciado sesión en la extensión de **GitHub Copilot**
- [ ] Panel de Chat abierto y Agent listo
<!-- track:vscode:end -->

<!-- track:cli:start -->
- [ ] GitHub Copilot CLI instalado y disponible como `copilot`
- [ ] Autenticado en la CLI con `/login`
- [ ] Cómodo usando comandos con barra como `/help`, `/plan` y `/review`
<!-- track:cli:end -->

> 💡 **Consejo:** Usa el DevContainer para un entorno preconfigurado si quieres empezar rápidamente en VS Code.

---

## 🧠 Lo que aprenderás

| # | Habilidad | Descripción |
|---|-----------|-------------|
| 1 | **Context Engineering** | Enséñale a Copilot sobre tu código con instrucciones, referencias y límites claros |
| 2 | **Plan First** | Redacta la arquitectura antes de implementar |
| 3 | **Implementación agéntica** | Deja que Copilot lleve a cabo trabajo de codificación en varios pasos con tu supervisión |
| 4 | **Diseño iterativo** | Usa Copilot para transformar los elementos visuales y refinar detalles de interacción |
| 5 | **Flujos de trabajo paralelos** | Divide el trabajo entre agentes, sesiones o tareas delegadas |

<!-- track:vscode:start -->
### Enfoque de funciones de VS Code

- **Chat + modo Ask** para exploración
- **Plan Mode** para solicitar arquitectura y diseño
- **Agent Mode** para implementación en varios archivos
- **Agentes locales y en la nube** para pulido en paralelo
<!-- track:vscode:end -->

<!-- track:cli:start -->
### Enfoque de funciones de Copilot CLI

- **Sesiones interactivas de CLI** con `copilot`
- **`/plan` y Shift+Tab** para planificación estructurada
- **Ediciones automáticas** con aprobaciones en línea y `/diff`
- **`/fleet`, `/delegate` y `/review`** para paralelismo y controles de calidad
<!-- track:cli:end -->

---

## 📚 Partes del taller

| Parte | Título | Descripción |
|------|--------|-------------|
| [**01**](01-setup.md) | Configuración y contexto | Crea tu repositorio, prepara tu entorno y dale a Copilot el contexto adecuado |
| [**02**](02-plan-and-scaffold.md) | Planificar y estructurar | Diseña la API y la arquitectura de la página antes de implementar |
| [**03**](03-agent-mode.md) | Construir el juego | Conecta la página de batalla y los gráficos de contribuciones con ayuda agéntica |
| [**04**](04-design-vibes.md) | Tematización centrada en el diseño | Convierte el esqueleto en una experiencia retro arcade |
| [**05**](05-polish.md) | Pulido y trabajo paralelo | Usa flujos multiagente para mejorar UX, robustez y calidad |
| [**06**](06-bonus.md) | Bonus y extensiones | Explora funciones abiertas, flujos de compartición y experimentos extra |

---

## 💡 Consejos pro

1. **Mantén el navegador abierto** — observa las actualizaciones en vivo mientras codificas.
2. **Haz commits con frecuencia** — guarda puntos de control limpios mientras iteras.
3. **Refina el plan antes de implementar** — mejores planes llevan a mejores resultados.
4. **Revisa los cambios de Copilot** — usa la vista de diferencias o las herramientas de revisión del CLI en lugar de aceptar a ciegas.

<!-- track:vscode:start -->
5. **Usa puntos de control y deshacer** en el chat si una iteración se desvía.
<!-- track:vscode:end -->

<!-- track:cli:start -->
5. **Usa `/session`, `/context` y `/share file`** cuando quieras inspeccionar o conservar tu trabajo.
<!-- track:cli:end -->
