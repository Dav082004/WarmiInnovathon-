# Warmi Innovathon 2026 · Kit para equipos

> Plantilla de repositorio para que cada equipo construya su solución al reto de la **ONG Ubuntu** con **Spec-Driven Development (SDD)**, **agentes de IA** y **GitHub**, en cuatro días y sin perder el control de lo que construye.
> Entrega: **domingo 15 de noviembre, 11:59 p. m.** · Final: **lunes 16**.

## Qué es esto

Es el punto de partida del repo de tu equipo. No trae una solución: trae **la forma de trabajar** para llegar a una.

- **SDD, la spec manda.** Antes de programar, el equipo escribe *qué* va a construir y *por qué* (`spec.md`). De la spec salen el plan, las tareas, los issues, el código y las pruebas. Si cambia la idea, primero cambia la spec.
- **Cinco agentes de IA con rol fijo** (Especificador, Planificador, Desarrollador, QA y Desplegador), para GitHub Copilot y para OpenCode, que siguen las mismas reglas que las personas.
- **Doce skills en español** que guían cada fase: de la idea a la spec, del plan a los issues, probar, abrir y revisar PRs, desplegar.
- **GitHub como mesa de trabajo:** issues por área, tablero en GitHub Projects, pull requests revisados por una compañera y una CI que corre las pruebas.
- **El agente conectado a GitHub (MCP)** para crear issues, mover tarjetas y abrir PRs pidiendo confirmación antes de cada acción.

La regla de fondo: **la IA propone, una persona decide.**

## Míralo funcionando: la demo

**[Warmi Mentoras](https://github.com/Dav082004/WarmiInnovatho-Demo)** es un repo creado con esta plantilla y llevado de la idea a la demo publicada ([verla en vivo](https://dav082004.github.io/WarmiInnovatho-Demo/)). Sirve para ver:

1. **Cómo se usa SDD:** la spec 001 (un directorio de mentoras) con sus requisitos en EARS, su plan, sus tareas y una prueba por requisito.
2. **Cómo se divide el trabajo:** la spec 002 (*Mi match*, sugerencias explicables en 3 preguntas) partida en tareas de una sola área, con dependencias, olas en paralelo y quién tomó qué.
3. **Cómo debería verse el README de tu equipo:** el suyo sigue la [plantilla de README](docs/PLANTILLA-README.md) al pie de la letra.

Además deja una tarea pendiente a propósito (compartir por WhatsApp) para recorrer el flujo completo en vivo en el taller.

## El recorrido en 4 pasos

| Paso | Quién | Dónde |
| --- | --- | --- |
| 1. Configurar la computadora | Todas | [Parte 1](#parte-1--configura-tu-computadora-paso-a-paso) de este README |
| 2. Crear el repo del equipo | Una persona | [Parte 2](#parte-2--crea-el-repo-del-equipo-una-persona) |
| 3. Encender el agente | Todas | [Paso 8](#paso-8-conecta-el-agente-con-github-mcp) de la Parte 1 |
| 4. Primera vuelta SDD | Todo el equipo | [Parte 3](#parte-3--el-flujo-sdd) y [docs/GUIA-INICIO.md](docs/GUIA-INICIO.md) |

---

## Parte 1 · Configura tu computadora, paso a paso

Al final de esta parte tendrás: Git, VS Code, Node.js, GitHub CLI, GitHub Copilot (con agentes, skills y el MCP de GitHub) y OpenCode de respaldo.

### Atajo: todo con un script

Si prefieres no instalar cada cosa a mano, descarga este repo (**Code → Download ZIP**, si aún no tienes Git), abre una terminal en su carpeta y corre:

```powershell
# Windows 10/11 (PowerShell). Usa winget.
powershell -ExecutionPolicy Bypass -File setup\instalar.ps1
```

```bash
# Mac (necesita Homebrew) o Linux (Ubuntu/Debian, usa apt)
bash setup/instalar.sh
```

El script instala lo que falta, se salta lo que ya tienes y se puede correr varias veces. Después sigue desde el [Paso 3](#paso-3-configura-git-con-tu-nombre-y-correo). Si algo queda como **FALTA**, cierra y abre la terminal y córrelo de nuevo (Windows actualiza el `PATH` solo en ventanas nuevas).

> 📖 [winget](https://learn.microsoft.com/es-es/windows/package-manager/winget/) · [Homebrew](https://brew.sh/)

### Paso 1. Cuenta de GitHub y beneficios de estudiante

**Para qué:** GitHub guarda el código del equipo, los issues, el tablero y la demo. Con **GitHub Education** tienes Copilot gratis como estudiante.

1. Crea tu cuenta en [github.com/signup](https://github.com/signup) (si ya tienes, salta este punto).
2. Si eres estudiante, solicita **GitHub Education** con tu correo o carné de estudiante. La aprobación puede tardar: mientras tanto sirve **Copilot Free**.

> 📖 [Crear una cuenta en GitHub](https://docs.github.com/es/get-started/start-your-journey/creating-an-account-on-github) · [Solicitar GitHub Education como estudiante](https://docs.github.com/es/education/about-github-education/github-education-for-students/apply-to-github-education-as-a-student) · [GitHub Student Developer Pack](https://education.github.com/pack)

### Paso 2. Instala Git

**Para qué:** guardar versiones de tu trabajo y compartirlas con el equipo.

1. Descárgalo de [git-scm.com/downloads](https://git-scm.com/downloads) e instala con las opciones por defecto. En Windows también: `winget install --id Git.Git -e`.
2. Comprueba en una terminal nueva:

```bash
git --version
```

> 📖 [Descargas de Git](https://git-scm.com/downloads) · [Libro Pro Git, en español](https://git-scm.com/book/es/v2)

### Paso 3. Configura Git con tu nombre y correo

**Para qué:** que cada commit diga quién lo hizo. Usa el **mismo correo de tu cuenta de GitHub**.

```powershell
# Windows
powershell -ExecutionPolicy Bypass -File setup\configurar-git.ps1
```

```bash
# Mac o Linux
bash setup/configurar-git.sh
```

O a mano:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo@ejemplo.com"
git config --global init.defaultBranch main
```

Comprueba con `git config --global --list`.

> 📖 [Configurando Git por primera vez](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Configurando-Git-por-primera-vez)

### Paso 4. Instala Visual Studio Code

**Para qué:** es el editor donde vive el agente de Copilot.

Descárgalo de [code.visualstudio.com/download](https://code.visualstudio.com/download). En Windows también: `winget install --id Microsoft.VisualStudioCode -e`.

> 📖 [Instalar VS Code](https://code.visualstudio.com/docs/setup/setup-overview)

### Paso 5. Instala Node.js (versión LTS)

**Para qué:** correr las pruebas y servidores de muchas tecnologías web, e instalar OpenCode.

1. Descarga la versión **LTS** de [nodejs.org/es/download](https://nodejs.org/es/download). En Windows también: `winget install --id OpenJS.NodeJS.LTS -e`.
2. Comprueba:

```bash
node --version
npm --version
```

> 📖 [Descargar Node.js](https://nodejs.org/es/download) · [Ejecutor de pruebas de Node (`node --test`)](https://nodejs.org/api/test.html)

### Paso 6. Instala GitHub CLI e inicia sesión

**Para qué:** iniciar sesión en GitHub desde la terminal y crear las etiquetas y el tablero del equipo con un comando.

1. Instálalo desde [cli.github.com](https://cli.github.com/). En Windows: `winget install --id GitHub.cli -e`. En Mac: `brew install gh`.
2. Inicia sesión (elige **GitHub.com**, **HTTPS** y **Login with a web browser**):

```bash
gh auth login
```

3. Solo la persona que creará el tablero, una vez: `gh auth refresh -s project`.
4. Comprueba con `gh auth status`.

> 📖 [GitHub CLI](https://cli.github.com/) · [`gh auth login`](https://cli.github.com/manual/gh_auth_login) · [Manual completo](https://cli.github.com/manual/)

### Paso 7. Activa GitHub Copilot en VS Code

**Para qué:** es el agente principal. Lee las reglas del repo (`AGENTS.md`), usa los agentes de `.github/agents/` y las skills de `.agents/skills/`.

1. En VS Code, abre el panel de **Extensiones** e instala **GitHub Copilot**, **GitHub Copilot Chat** y **GitHub Pull Requests**. Al abrir este repo, VS Code te las sugiere solo.
2. Inicia sesión con tu cuenta de GitHub: icono de **Cuentas** (abajo a la izquierda) → *Sign in with GitHub to use GitHub Copilot*.
3. Abre el chat (`Ctrl+Alt+I` en Windows/Linux, `⌃⌘I` en Mac) y cambia el modo a **Agent**.
4. Con este repo abierto, en el selector de agentes aparecen **Especificador, Planificador, Desarrollador, QA y Desplegador**.

> 📖 [Configurar Copilot en VS Code](https://code.visualstudio.com/docs/copilot/setup) · [Modo agente](https://code.visualstudio.com/docs/copilot/chat/chat-agent-mode) · [Agentes personalizados](https://code.visualstudio.com/docs/copilot/customization/custom-agents) · [Agent Skills](https://code.visualstudio.com/docs/copilot/customization/agent-skills) · [Documentación de GitHub Copilot](https://docs.github.com/es/copilot) · [Qué es `AGENTS.md`](https://agents.md/)

### Paso 8. Conecta el agente con GitHub (MCP)

**Para qué:** que el agente pueda leer y crear issues, mover tarjetas del tablero, abrir pull requests y ver la CI. Ya viene configurado en [`.vscode/mcp.json`](.vscode/mcp.json).

1. Abre la carpeta del repo en VS Code (`code .`).
2. Abre `.vscode/mcp.json` y pulsa **Start** sobre el servidor `github`. Autoriza con tu cuenta. Si no ves **Start**: `Ctrl+Shift+P` → **MCP: List Servers**.
3. En el chat, modo **Agent**, pulsa el icono de herramientas y confirma que aparecen las de GitHub.
4. Prueba: *"¿Qué issues abiertos hay en este repo?"*

El agente **te pedirá confirmación** antes de cambiar algo en GitHub. Lee qué va a hacer antes de aceptar.

> 📖 [Servidores MCP en VS Code](https://code.visualstudio.com/docs/copilot/customization/mcp-servers) · [Servidor MCP de GitHub](https://github.com/github/github-mcp-server)

### Paso 9. OpenCode, el agente de respaldo

**Para qué:** si se acaba la cuota de Copilot, seguir trabajando desde la terminal con los mismos agentes, reglas y skills.

1. Instálalo: `npm install -g @opencode/cli` (en Mac o Linux, si da error de permisos, antepón `sudo`).
2. Crea un **token personal** en GitHub (**Settings → Developer settings → Personal access tokens**) con permisos de `repo` y `project`.
3. Guárdalo en la variable de entorno `GITHUB_TOKEN`, **nunca en un archivo del repo**:
   - Windows: `[Environment]::SetEnvironmentVariable("GITHUB_TOKEN", "pega-tu-token", "User")` y abre una terminal nueva.
   - Mac o Linux: agrega `export GITHUB_TOKEN=pega-tu-token` a `~/.zshrc` o `~/.bashrc`.
4. En la carpeta del repo: `opencode`. La primera vez, `/connect` para elegir el proveedor de modelos (por ejemplo GitHub Copilot). Elige el agente con `/agents`.
5. Comprueba el MCP con `opencode mcp list`: debe aparecer `github`.

> 📖 [Documentación de OpenCode](https://opencode.ai/docs/) · [Agentes](https://opencode.ai/docs/agents/) · [Skills](https://opencode.ai/docs/skills/) · [Servidores MCP](https://opencode.ai/docs/mcp-servers/) · [Tokens personales de GitHub](https://docs.github.com/es/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

### Paso 10. Comprueba que todo está listo

```powershell
powershell -ExecutionPolicy Bypass -File setup\verificar.ps1   # Windows
```

```bash
bash setup/verificar.sh                                         # Mac o Linux
```

Revisa cada herramienta, tu configuración de Git y la sesión de GitHub, y te dice el siguiente paso para lo que falte. Problemas frecuentes y sus soluciones: [docs/INSTALACION.md](docs/INSTALACION.md#si-algo-falla).

### Resumen: qué se instala y dónde está su documentación

| Herramienta | Para qué | Obligatoria | Documentación oficial |
| --- | --- | --- | --- |
| Cuenta de GitHub | Código, issues, tablero y demo | Sí | [docs.github.com](https://docs.github.com/es/get-started/start-your-journey/creating-an-account-on-github) |
| GitHub Education | Copilot gratis para estudiantes | Recomendada | [education.github.com](https://docs.github.com/es/education/about-github-education/github-education-for-students/apply-to-github-education-as-a-student) |
| Git | Versiones y trabajo en equipo | Sí | [git-scm.com/book/es](https://git-scm.com/book/es/v2) |
| VS Code | Editor con el agente | Sí (o tu editor) | [code.visualstudio.com/docs](https://code.visualstudio.com/docs/setup/setup-overview) |
| Node.js LTS | Pruebas, servidores, OpenCode | Recomendada | [nodejs.org](https://nodejs.org/es/download) |
| GitHub CLI | Sesión, etiquetas y tablero por comandos | Recomendada | [cli.github.com/manual](https://cli.github.com/manual/) |
| GitHub Copilot | Agente principal | Una de las dos | [Copilot en VS Code](https://code.visualstudio.com/docs/copilot/setup) |
| MCP de GitHub | El agente trabaja en GitHub | Recomendada | [github-mcp-server](https://github.com/github/github-mcp-server) |
| OpenCode | Agente de respaldo en la terminal | Una de las dos | [opencode.ai/docs](https://opencode.ai/docs/) |

Las herramientas son de libre elección: si tu equipo prefiere otro editor, otro lenguaje u otro agente, las reglas de `AGENTS.md` y las skills siguen valiendo.

---

## Parte 2 · Crea el repo del equipo (una persona)

1. **Crea el repo desde esta plantilla:** botón **Use this template → Create a new repository**. Que sea **público**.
   > 📖 [Crear un repositorio desde una plantilla](https://docs.github.com/es/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
2. **Invita al equipo:** **Settings → Collaborators → Add people**.
   > 📖 [Gestionar quién tiene acceso](https://docs.github.com/es/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository)
3. **Pon el README del equipo** en lugar de este. Clona el repo y corre:

   ```bash
   git mv -f docs/PLANTILLA-README.md README.md
   git commit -m "docs: usa la plantilla de README del equipo"
   git push
   ```

   Este README (el del kit) siempre se puede consultar en el repo original.
4. **Crea las etiquetas por área** (`área: diseño`, `área: frontend`, `área: backend-datos`, `área: pruebas`, `área: despliegue`, `área: docs-pitch`):

   ```bash
   bash setup/crear-etiquetas.sh                                        # Mac o Linux
   powershell -ExecutionPolicy Bypass -File setup\crear-etiquetas.ps1   # Windows
   ```

   > 📖 [Administrar etiquetas](https://docs.github.com/es/issues/using-labels-and-milestones-to-track-work/managing-labels)
5. **Crea el tablero** con columnas *Por hacer, En progreso, En revisión, Hecho* y los campos *Área*, *RF* y *Tarea* (paso a paso en [docs/ISSUES-Y-TABLERO.md](docs/ISSUES-Y-TABLERO.md), o con `setup/crear-tablero`).
   > 📖 [Inicio rápido de GitHub Projects](https://docs.github.com/es/issues/planning-and-tracking-with-projects/learning-about-projects/quickstart-for-projects) · [Sub-issues](https://docs.github.com/es/issues/tracking-your-work-with-issues/using-issues/adding-sub-issues) · [`gh project`](https://cli.github.com/manual/gh_project)
6. **Protege `main`:** **Settings → Branches** → exige pull request con una aprobación.
   > 📖 [Ramas protegidas](https://docs.github.com/es/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches)
7. **Cuando tengan algo que mostrar**, activa la demo: **Settings → Pages → Source: GitHub Actions** (el agente Desplegador escribe el workflow).
   > 📖 [Configurar la publicación de GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) · [GitHub Actions](https://docs.github.com/es/actions)

El resto del equipo: `git clone https://github.com/<usuario>/<repo>.git`, Paso 3 de la Parte 1 si aún no lo hicieron, y abrir la carpeta en VS Code.

---

## Parte 3 · El flujo SDD

```
Constitución → Spec → Clarificación → Plan → Tareas e issues → Desarrollo + pruebas → Despliegue → Pitch
                 ↑                                                                         │
                 └───────────── ¿cambió algo? primero se actualiza la spec ────────────────┘
```

| Fase | Agente | Qué le dices | Queda en |
| --- | --- | --- | --- |
| Requisitos | Especificador | *"Queremos construir [idea]. Entrevístanos y escribe la spec."* | `specs/001-.../spec.md` |
| Clarificación | QA | *"Revisa la spec 001 como QA. Solo detecta, no resuelvas."* | la spec corregida |
| Plan y tareas | Planificador | *"La spec 001 está aprobada. Escribe el plan y las tareas, y crea los issues por área."* | `plan.md`, `tasks.md`, tablero |
| Reparto | **El equipo** | 10 minutos frente al tablero: cada una se asigna sus issues | el tablero |
| Desarrollo | Desarrollador | *"Tomé el issue #N. Implementa solo esa tarea, pruebas primero."* | rama, commits y PR |
| Revisión | QA y una compañera | *"Ayúdame a revisar el PR #N."* | merge a `main` |
| Despliegue | Desplegador | *"Publica la demo y deja el enlace en el README."* | enlace a la demo |

Todo el detalle: [docs/FLUJO-SDD.md](docs/FLUJO-SDD.md) · Primeros 15 minutos: [docs/GUIA-INICIO.md](docs/GUIA-INICIO.md).

## Qué trae esta plantilla

| Carpeta o archivo | Para qué |
| --- | --- |
| [`docs/PLANTILLA-README.md`](docs/PLANTILLA-README.md) | El README de tu equipo, listo para completar |
| [`docs/GUIA-INICIO.md`](docs/GUIA-INICIO.md) | Los primeros 15 minutos, paso a paso |
| [`docs/INSTALACION.md`](docs/INSTALACION.md) y `setup/instalar.*` | Instalación con script y solución de problemas |
| [`docs/COMANDOS-GIT.md`](docs/COMANDOS-GIT.md) | Los comandos de Git que hay que conocer y qué hacer cuando algo sale mal |
| [`docs/USAR-SPEC.md`](docs/USAR-SPEC.md) | Cómo escribir y usar la spec, con requisitos en notación EARS |
| [`docs/ISSUES-Y-TABLERO.md`](docs/ISSUES-Y-TABLERO.md) | Issues, etiquetas por área y tablero de GitHub Projects |
| [`docs/EJEMPLO-TAREA.md`](docs/EJEMPLO-TAREA.md) | Una tarea dividida por áreas, de la spec a *Hecho* |
| [`docs/FLUJO-SDD.md`](docs/FLUJO-SDD.md) | El flujo completo y qué decirle al agente en cada fase |
| [`docs/constitution.md`](docs/constitution.md) | Los principios del proyecto |
| [`docs/pitch.md`](docs/pitch.md) | Guion para la exposición |
| [`docs/SKILLS-EXTRA.md`](docs/SKILLS-EXTRA.md) | Más skills y herramientas opcionales |
| [`specs/000-plantilla/`](specs/000-plantilla/) | Plantillas de spec, plan y tareas |
| [`setup/`](setup/) | Instalar, configurar Git, verificar, y crear etiquetas y tablero |
| [`.github/agents/`](.github/agents/) y [`.opencode/agents/`](.opencode/agents/) | Los cinco agentes con rol fijo |
| [`.agents/skills/`](.agents/skills/) | Las doce skills del flujo |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/) y plantilla de PR | Issues y PRs ordenados |
| [`.github/workflows/ci.yml`](.github/workflows/ci.yml) | Corre las pruebas en cada pull request (Node o Python) |
| [`.vscode/mcp.json`](.vscode/mcp.json) y [`opencode.json`](opencode.json) | Conectan el agente con GitHub |
| [`AGENTS.md`](AGENTS.md) y [`CONTRIBUTING.md`](CONTRIBUTING.md) | Las reglas, para la IA y para las personas |

## Para profundizar en SDD

- [mouredev/hello-sdd](https://github.com/mouredev/hello-sdd): curso en español de Spec-Driven Development (el formato de la spec y los prompts por fase se adaptaron de aquí).
- [GitHub Spec Kit](https://github.com/github/spec-kit): el kit de GitHub para trabajar con specs y agentes.

> Los enlaces de documentación se revisaron el 12 de noviembre de 2026. Las herramientas cambian: si un paso no coincide con lo que ves, la documentación oficial enlazada en ese paso manda.

---

Hecha para la Warmi Innovathon 2026, con el apoyo de Ubuntu, Makipuray, Microsoft y GitHub Education. Licencia en [LICENSE](LICENSE) y créditos de las skills en [NOTICE.md](NOTICE.md).
