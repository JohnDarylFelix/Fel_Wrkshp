<!-- l10n-sync: source-file="workshop/01-setup.md" -->
# Parte 1: Configuración y contexto

---

En esta parte configurarás tu entorno de desarrollo **y** enseñarás a Copilot sobre la base de código para que cada prompt futuro empiece con el contexto correcto.

## Sección 1: Configuración inicial

### Paso 1: Crea tu repositorio

1. Abre [github.com/copilot-dev-days/mona-mayhem](https://github.com/copilot-dev-days/mona-mayhem)
2. Crea tu propio repositorio usando cualquiera de estas opciones:
   - haciendo clic en **Use this template** → **Create a new repository**, o
   - haciendo fork del repositorio.
3. Nómbralo `my-mona-mayhem` y configura la visibilidad como **Public** (si lo creaste desde la plantilla)

<!-- track:vscode:start -->
### Paso 2: Elige tu entorno de desarrollo

#### Opción A: VS Code local

1. Abre VS Code y ejecuta **Git: Clone** → **Clone from GitHub**
2. Selecciona tu repositorio `my-mona-mayhem`
3. Cuando se te pregunte, instala las **extensiones recomendadas**

#### Opción B: GitHub Codespaces

1. Abre tu repositorio en GitHub
2. Haz clic en **Code** → **Codespaces** → **Create codespace on main**
3. Espera a que el entorno se inicie y a que se instalen las dependencias

### Paso 3: Instala dependencias y arranca la app

1. Abre el terminal integrado en tu repositorio.
2. Instala las dependencias:

   ```bash
   npm install
   ```

3. Inicia la app:

   ```bash
   npm run dev
   ```

> ✅ **La app está funcionando en tu navegador.**
<!-- track:vscode:end -->

<!-- track:cli:start -->
### Paso 2: Instala GitHub Copilot CLI

Usa la ruta de instalación que corresponda a tu máquina:

- **npm (multiplataforma, requiere Node.js 22+)**

  ```bash
  npm install -g @github/copilot
  ```

- **Homebrew (macOS/Linux)**

  ```bash
  brew install copilot-cli
  ```

- **WinGet (Windows)**

  ```bash
  winget install GitHub.Copilot
  ```

### Paso 3: Inicia la app y autentica la CLI

1. Clona tu repositorio localmente y abre una terminal en la raíz del proyecto.
2. Instala las dependencias e inicia la app:

   ```bash
   npm install
   npm run dev
   ```

3. Abre un **segundo terminal** en el mismo repositorio y arranca Copilot CLI:

   ```bash
   copilot
   ```

4. En la sesión interactiva, escribe:

   ```
   /login
   ```

5. Sigue las indicaciones del flujo del dispositivo y confirma que confías en el repositorio cuando la CLI te pida aprobación.

> ✅ **Ya tienes la vista previa de la app en un terminal y Copilot CLI listo en otro.**
<!-- track:cli:end -->

## Sección 2: Ingeniería de contexto

La ingeniería de contexto consiste en enseñar a la IA sobre tu base de código. Cuanto mejor sea el contexto, mejor será cada respuesta futura.

<!-- track:vscode:start -->
### Tarea 1: Genera instrucciones del espacio de trabajo con /init

Vamos a usar el comando integrado `/init` para generar un archivo de instrucciones del espacio de trabajo para Copilot:

1. Abre **Copilot Chat** y escribe:

   ```
   /init simple instructions with a project overview, build/dev commands, and Astro best practices, (ignore the workshop).
   ```

2. Revisa el archivo generado: Copilot analizará tu proyecto y creará un `.github/copilot-instructions.md`.
3. Acepta los cambios y luego **haz commit** del archivo de instrucciones.

> **Resultado:** Todas las futuras peticiones a Copilot tendrán un mapa del espacio de trabajo integrado.

### Tarea 2: Agentes en segundo plano

**Agente local en segundo plano:**

1. En el panel de chat, haz clic en **+** para crear un chat nuevo
2. En la parte inferior de la ventana verás **Local** cambiar a **Copilot CLI**
3. Introduce el siguiente prompt:

   > "Add linting rules for unused vars and improve code style; fix any errors"

4. Cuando termine, **Revisa y aplica** los cambios y, si quieres, archiva la sesión.

**Agente en la nube:**

1. En el panel de chat, haz clic en **+** para crear un chat nuevo
2. En la parte inferior de la ventana verás **Local** cambiar a **Cloud**

   > "Make the README more engaging as a landing page"

> **Resultado:** Reglas de linting añadidas, errores corregidos y README mejorado, todo sin salir del editor.

### Tarea 3: Explora el proyecto

Abre **Copilot Chat** en **Ask mode** y prueba estos prompts:

- `"Explain the architecture of this project"`
- `"What files are in the src directory and what do they do?"`
- `"What would I need to build to make the Battle button work?"`

> 💡 Usa **@workspace** para dar a Copilot contexto de todo el proyecto y obtener respuestas más precisas.
<!-- track:vscode:end -->

<!-- track:cli:start -->
### Tarea 1: Genera instrucciones del repositorio con /init

Vamos a usar `/init` para generar un archivo de instrucciones para Copilot:

1. En Copilot CLI, escribe:

   ```
   /init simple instructions with a project overview, build/dev commands, and Astro best practices, (ignore the workshop).
   ```

2. Revisa el archivo generado: Copilot analizará tu proyecto y creará un `.github/copilot-instructions.md`.
3. Haz commit del archivo de instrucciones.

> **Resultado:** Las futuras sesiones de CLI heredan automáticamente instrucciones específicas del repositorio desde `.github/copilot-instructions.md`.

### Tarea 2: Ajusta tu entorno CLI

Practica los controles de la CLI que hacen más fluidos los siguientes pasos:

1. Ejecuta `/help` para revisar los comandos disponibles.
2. Usa `/model` para ver los modelos disponibles para ti.
3. Si Copilot ha aprendido demasiadas aprobaciones durante la experimentación, restablécelas con:

   ```
   /reset-allowed-tools
   ```

4. Si tu repositorio vive dentro de un directorio padre más grande, usa `/add-dir PATH` para ampliar explícitamente el espacio de trabajo permitido.

> 💡 La documentación de la CLI recomienda instrucciones personalizadas breves y permisos explícitos para que Copilot siga siendo rápido y predecible.

### Tarea 3: Explora el proyecto desde la terminal

Prueba estos prompts dentro de Copilot CLI:

- `Give me an overview of this project.`
- `@src/pages/api/contributions/[username].ts What is this file for and what needs to be built here?`
- `@src/pages/index.astro What exists here and what would I need to add to build the battle page?`

Si quieres una respuesta rápida en un único paso fuera de la sesión interactiva, prueba:

```bash
copilot -p "Summarize the architecture of this repo in 5 bullet points"
```

> **Resultado:** Ya tienes instrucciones, conocimiento de comandos y una idea de cómo introducir archivos en el contexto de Copilot CLI.
<!-- track:cli:end -->

## ✅ Parte 1 completada

Has aprendido a:

- **Configurar** el repositorio y el entorno de desarrollo local
- **Generar instrucciones** con `/init` para que Copilot entienda tu proyecto y la dirección del diseño
- **Establecer un hábito de revisión** antes de aplicar cambios generados
- **Explorar la base de código** con prompts ricos en contexto
