<!-- l10n-sync: source-file="README.md" -->
🌐 [English](README.md) | Español | [Português (Brasil)](README.pt_BR.md) | [한국어](README.ko.md)

# 🎮 Mona Mayhem

**Taller de VS Code & GitHub Copilot CLI** — Crea una arena de batalla de contribuciones de GitHub

Un modelo de taller para crear un sitio web retro arcade con Astro que compara los gráficos de contribución de GitHub de dos usuarios. Este es el **punto de partida** — construirás la app paso a paso usando GitHub Copilot.

![Mona Mayhem Screenshot](https://github.com/user-attachments/assets/5eca79e2-cb9f-4e93-aa0d-23666ebde3b7)
*Lo que construirás al final del taller*

## 📚 Taller

El taller admite dos rutas: sigue la que coincida con tu flujo de trabajo preferido:

- **Ruta de VS Code** — Chat, Plan Mode, Agent Mode, agentes en segundo plano y bucles de revisión nativos del editor
- **Ruta de CLI** — `copilot`, contexto con `@file`, `/plan`, ediciones autónomas, `/fleet`, `/delegate` y `/review`

| Parte | Título | Enfoque de Copilot |
|------|--------|--------------------|
| [00](workshop/es/00-overview.md) | Visión general | Selección de ruta y objetivos de aprendizaje |
| [01](workshop/es/01-setup.md) | Configuración y contexto | Instrucciones, permisos y configuración del entorno |
| [02](workshop/es/02-plan-and-scaffold.md) | Planificación y estructura | Planificación de la API y la arquitectura de la página |
| [03](workshop/es/03-agent-mode.md) | Crear el juego | Implementación y iteración agéntica |
| [04](workshop/es/04-design-vibes.md) | Tematización centrada en el diseño | Planificación e implementación visual |
| [05](workshop/es/05-polish.md) | Pulido y trabajo paralelo | Paralelismo, revisiones y pasadas de calidad |
| [06](workshop/es/06-bonus.md) | Bonus y extensiones | Ideas de funciones abiertas y experimentos extra de Copilot |

## 🚀 Inicio rápido

1. **Crea primero tu propio repositorio** mediante cualquiera de estas opciones:
   - haciendo clic en **Use this template** para crear un nuevo repositorio, o
   - bifurcando este repositorio.
2. Elige tu camino del taller:
   - **VS Code:** clona tu repositorio y ábrelo en VS Code.
   - **GitHub Copilot CLI:** clona tu repositorio localmente, instala `copilot` y trabaja desde tu terminal.
3. Sigue la [guía del taller](workshop/es/00-overview.md)

## Requisitos previos

### Compartidos

- GitHub Copilot (Pro, Business o Enterprise)
- Git
- Node.js

### Ruta de VS Code

- VS Code v1.107+
- Extensión de GitHub Copilot iniciada sesión

### Ruta de CLI

- GitHub Copilot CLI (`copilot`)
- Node.js 22+ si planeas instalar la CLI con `npm install -g @github/copilot`
- O Homebrew / WinGet si prefieres un gestor de paquetes nativo

## Stack tecnológico

- **Framework**: [Astro](https://astro.build/) v6
- **Runtime**: Node.js con el adaptador [@astrojs/node](https://docs.astro.build/en/guides/integrations-guide/node/)
- **Fuente**: Press Start 2P (fuente retro de videojuegos)
- **API**: API de gráficos de contribución de GitHub

## Notas de despliegue

### Configuración actual de GitHub Pages

El flujo de trabajo en `.github/workflows/deploy.yml` despliega actualmente el contenido estático del taller de `docs/` y `workshop/` en GitHub Pages. No compila ni despliega la app Astro desde `src/`.

### Si quieres desplegar la app Astro en GitHub Pages

GitHub Pages es un alojamiento estático, por lo que la app Astro debería usar salida estática.

1. Cambia `output` en `astro.config.mjs` de `server` a `static`.
2. Elimina el adaptador de Node (`@astrojs/node`) de `astro.config.mjs` y `package.json`.
3. Actualiza el flujo de trabajo de GitHub Actions para ejecutar `npm ci` y `npm run build`, y luego subir `dist/` como artefacto de Pages.
4. Si despliegas en una página de proyecto (`https://<user>.github.io/<repo>/`), establece `site` y `base` en `astro.config.mjs`.

Si planeas mantener las rutas de la API ejecutándose en producción, usa una plataforma de servidor en su lugar (por ejemplo, Vercel, Netlify o un host de Node).

## Licencia

MIT
