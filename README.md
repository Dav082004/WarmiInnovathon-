# [Nombre del proyecto]

> **Warmi Innovathon 2026** · Reto planteado por la ONG Ubuntu
> Equipo: **[nombre del equipo]** · Mentora: **[nombre]**

<!--
  Esta es la plantilla de tu equipo. Reemplaza todo lo que está entre [corchetes]
  y borra este comentario. ¿Primera vez? Empieza por docs/GUIA-INICIO.md
-->

## El problema

[En 3 a 5 líneas: ¿qué problema plantea Ubuntu? ¿A quién afecta? ¿Por qué importa?]

## Nuestra solución

[En 3 a 5 líneas: ¿qué construimos y cómo resuelve el problema?]

**¿Para quién es?** [usuaria principal]

**¿Qué la hace distinta?** [la propuesta de valor]

## Demo

[Enlace a la demo desplegada, y un video o capturas de pantalla]

## Funcionalidades

- [ ] [Funcionalidad 1]
- [ ] [Funcionalidad 2]
- [ ] [Funcionalidad 3]

El detalle está en la spec: [`specs/001-.../spec.md`](specs/).

## Tecnologías

| Parte | Herramienta |
| --- | --- |
| Frontend | [ ] |
| Backend / datos | [ ] |
| Despliegue | [ ] |
| IA | [GitHub Copilot / OpenCode] + MCP de GitHub |

## Cómo ejecutarlo

```bash
git clone https://github.com/[usuario]/[repo].git
cd [repo]
[comando para instalar]
[comando para ejecutar]
[comando para correr las pruebas]
```

## Equipo

| Nombre | Rol | GitHub |
| --- | --- | --- |
| [Nombre] | [ ] | [@usuario] |
| [Nombre] | [ ] | [@usuario] |
| [Nombre] | [ ] | [@usuario] |
| [Nombre] | [ ] | [@usuario] |

## Cómo trabajamos

Usamos **Spec-Driven Development**: primero acordamos qué construir en una spec, y de ahí salen el plan, las tareas, el código y las pruebas. El recorrido completo está en [docs/FLUJO-SDD.md](docs/FLUJO-SDD.md).

- `main` siempre funciona, y todo entra por pull request revisado por una compañera.
- Una tarea = un issue = una rama. El tablero dice quién hace qué.
- La IA propone, una persona decide.

Reglas completas: [CONTRIBUTING.md](CONTRIBUTING.md) para personas y [AGENTS.md](AGENTS.md) para la IA.

## Qué trae esta plantilla

| Carpeta o archivo | Para qué |
| --- | --- |
| `docs/GUIA-INICIO.md` | Los primeros 15 minutos, paso a paso |
| `docs/INSTALACION.md` y `setup/instalar.*` | Instalar Git, VS Code, Node, GitHub CLI, OpenCode y Copilot, con scripts para Windows, Mac y Linux |
| `docs/USAR-SPEC.md` | Cómo escribir y usar la spec, paso a paso |
| `docs/ISSUES-Y-TABLERO.md` | Issues, etiquetas por área y tablero de GitHub Projects, paso a paso |
| `docs/EJEMPLO-TAREA.md` | Una tarea de ejemplo dividida por áreas, de la spec a *Hecho* |
| `docs/FLUJO-SDD.md` | El flujo completo y qué decirle al agente en cada fase |
| `docs/constitution.md` | Los principios del proyecto |
| `specs/000-plantilla/` | Plantillas de spec, plan y tareas |
| `setup/` | Scripts para instalar las herramientas, configurar Git y crear las etiquetas |
| `.github/agents/` y `.opencode/agents/` | Cinco agentes con rol fijo: Especificador, Planificador, Desarrollador, QA y Desplegador |
| `.agents/skills/` | Doce skills en español para el flujo |
| `.github/ISSUE_TEMPLATE/` y plantilla de PR | Issues y PRs ordenados |
| `.github/workflows/ci.yml` | Corre las pruebas en cada pull request |
| `.vscode/mcp.json` y `opencode.json` | Conectan el agente con GitHub (issues, PRs, Projects) |
| `docs/pitch.md` | Guion para la exposición |
| `docs/SKILLS-EXTRA.md` | Más skills y herramientas opcionales |

## Checklist de entrega (domingo 15, 11:59 p. m.)

- [ ] README completo (problema, solución, demo, equipo)
- [ ] `main` funciona: se puede clonar y ejecutar con los pasos de arriba
- [ ] Cada requisito de la spec tiene su prueba y la CI está en verde
- [ ] Todas las integrantes tienen al menos un PR revisado y fusionado
- [ ] Enlace a la demo funcionando
- [ ] Sin contraseñas, claves ni datos personales reales en el repo
- [ ] Repositorio público
- [ ] `docs/pitch.md` listo para la final del lunes 16

---

Hecha para la Warmi Innovathon, con el apoyo de Ubuntu, Makipuray, Microsoft y GitHub Education. Créditos de las skills en [NOTICE.md](NOTICE.md).
