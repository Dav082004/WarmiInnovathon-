# Guía de inicio (15 minutos)

## 1. Instala las herramientas

Necesitas Git, VS Code, Node, GitHub CLI, y un agente (GitHub Copilot, con OpenCode de respaldo). Hay un script que lo instala todo:

```bash
# Mac o Linux
bash setup/instalar.sh
```

```powershell
# Windows (PowerShell)
powershell -ExecutionPolicy Bypass -File setup\instalar.ps1
```

Los scripts viven en el repo. Si todavía no tienes Git para clonarlo, en GitHub usa **Code → Download ZIP**, descomprime y corre el script desde esa carpeta.

Qué instala, instalación a mano y cómo resolver problemas: [INSTALACION.md](INSTALACION.md). Si eres estudiante, verifica [GitHub Education](https://education.github.com/) para tener Copilot Student; mientras tanto sirve Copilot Free.

Las herramientas son de libre elección. Si tu equipo prefiere otro editor u otro agente, las reglas de `AGENTS.md` y las skills siguen sirviendo.

## 2. Crea el repo del equipo (solo una persona)

1. En el repositorio plantilla, botón **Use this template** → **Create a new repository**. Que sea **público**. (También pueden hacer un fork.)
2. **Settings → Collaborators** → invita al resto del equipo.
3. Crea las etiquetas (`setup/crear-etiquetas`) y el tablero, siguiendo [ISSUES-Y-TABLERO.md](ISSUES-Y-TABLERO.md).
4. Recomendado: **Settings → Branches** → protege `main` para exigir pull request con una aprobación.

## 3. Clona y configura Git (todas)

```bash
git clone https://github.com/<usuario>/<repo>.git
cd <repo>
```

Configura Git con el script:

```bash
# Mac o Linux
bash setup/configurar-git.sh
```

```powershell
# Windows (PowerShell)
powershell -ExecutionPolicy Bypass -File setup\configurar-git.ps1
```

Te pide tu nombre y tu correo de GitHub, y deja `main` como rama por defecto.

## 4. Enciende el agente

El detalle del MCP (y del token para OpenCode) está en [INSTALACION.md](INSTALACION.md#conectar-el-agente-con-github-mcp).

**Con GitHub Copilot en VS Code**

1. Abre la carpeta del repo en VS Code (`code .`).
2. Abre `.vscode/mcp.json` y haz clic en **Start** sobre el servidor `github`. Autoriza con tu cuenta.
3. Abre el chat de Copilot, cambia el modo a **Agent** y elige un agente del selector (Especificador, Planificador…).
4. Prueba: *"¿Qué issues abiertos hay en este repo?"*

**Con OpenCode (respaldo)**

1. Crea un token en GitHub: **Settings → Developer settings → Personal access tokens** (permisos de repo y project).
2. Guárdalo en la variable de entorno `GITHUB_TOKEN`. Nunca lo escribas en un archivo del repo.
3. Ejecuta `opencode` en la carpeta del repo y cambia de agente con `Tab`.

Los dos leen las mismas reglas (`AGENTS.md`) y las mismas skills (`.agents/skills/`). Si tu agente no detecta las skills, copia esa carpeta a `.github/skills/` (Copilot) o `.opencode/skills/` (OpenCode).

**Sin MCP** todo se puede hacer igual desde la web de GitHub.

## 5. Tu primera vuelta completa

1. **Especificador:** *"Queremos construir [idea]. Entrevístanos y escribe la spec."* → `specs/001-.../spec.md`, a `main` por PR.
2. **QA:** *"Revisa la spec como QA."* → corrigen lo que haga falta.
3. **Planificador:** *"Escribe el plan y las tareas, y crea los issues en el tablero."*
4. **El equipo** se reparte los issues.
5. **Desarrollador:** *"Tomé el issue #N. Implementa solo esa tarea, pruebas primero."* y luego *"Abre el PR."*
6. Una compañera revisa (con ayuda de **QA**) y hace merge.
7. **Desplegador:** *"Publica la demo."*

El detalle de cada fase está en [FLUJO-SDD.md](FLUJO-SDD.md); cómo escribir la spec, en [USAR-SPEC.md](USAR-SPEC.md); issues y tablero, en [ISSUES-Y-TABLERO.md](ISSUES-Y-TABLERO.md); y un ejemplo completo en [EJEMPLO-TAREA.md](EJEMPLO-TAREA.md).

## Si algo sale mal

- **Conflicto al fusionar:** no borres nada. Pídele al agente que te explique el conflicto antes de resolverlo, o pide ayuda a tu mentora.
- **Subí algo a `main` por error:** avisa al equipo. Se revierte con un PR, no borrando historia.
- **Subí una clave:** avisa de inmediato, cámbiala en el servicio y luego se limpia del repo.
- **La IA hizo algo que no pedí:** revisa que la spec lo diga claro. Si no está en la spec, ese es el arreglo.
