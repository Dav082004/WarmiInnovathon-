# [Nombre del proyecto]

> **Warmi Innovathon 2026** · Reto planteado por la ONG Ubuntu
> Equipo: **[nombre del equipo]** · Mentora: **[nombre]** · Demo: **[enlace]**

<!--
  PLANTILLA DEL README DE TU EQUIPO
  1. Conviértela en el README del repo (una sola persona, una sola vez):
       git mv -f docs/PLANTILLA-README.md README.md
     o, desde la web: copia este archivo, pégalo en README.md y borra este.
  2. Reemplaza todo lo que está entre [corchetes] y borra este comentario.
  3. Casi todo sale de la spec: no lo inventes aquí, cópialo de specs/001-.../spec.md.
  4. Guarda una captura de tu demo en docs/captura.png.
  (Los enlaces de este archivo apuntan desde la raíz del repo: funcionan cuando ya es README.md.)
  Un ejemplo completo: https://github.com/Dav082004/WarmiInnovatho-Demo
-->

![Captura de [nombre del proyecto]](docs/captura.png)

## El problema

[En 3 a 5 líneas: ¿qué problema plantea Ubuntu? ¿A quién afecta? ¿Por qué importa? Sale de "Contexto y objetivo" de la spec.]

## Nuestra solución

[En 3 a 5 líneas: ¿qué construimos y cómo resuelve el problema?]

**¿Para quién es?** [usuaria principal y desde qué dispositivo entra]

**¿Qué la hace distinta?** [la propuesta de valor de la spec]

## Demo

**[enlace a la demo publicada]**

Pruébala en 3 pasos:

1. [ ]
2. [ ]
3. [ ]

## Funcionalidades

Cada una con los requisitos (RF) de la spec que cumple.

- [ ] [Funcionalidad 1] (RF-1)
- [ ] [Funcionalidad 2] (RF-2, RF-3)
- [ ] [Funcionalidad 3] (RF-4)

El detalle está en la spec: [`specs/001-.../spec.md`](specs/).

## Tecnologías

| Parte | Herramienta |
| --- | --- |
| Frontend | [ ] |
| Backend / datos | [ ] |
| Pruebas | [ ] |
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

## Cómo lo construimos

Usamos **Spec-Driven Development**: primero acordamos qué construir en una spec, y de ahí salen el plan, las tareas, el código y las pruebas.

| Fase | Dónde quedó |
| --- | --- |
| Principios | [docs/constitution.md](docs/constitution.md) |
| Requisitos | [`specs/001-.../spec.md`](specs/) |
| Plan y tareas | [`plan.md`](specs/) y [`tasks.md`](specs/) |
| Código | [ ] |
| Pruebas | [ ] y la [CI](.github/workflows/ci.yml) |
| Despliegue | [ ] |
| Pitch | [docs/pitch.md](docs/pitch.md) |

| Spec | Qué agrega | RF | Estado |
| --- | --- | --- | --- |
| [001-…](specs/) | [ ] | RF-1 a RF-[n] | [aprobada / implementada] |

## Cómo nos dividimos el trabajo

Tablero: **[enlace al tablero de GitHub Projects]**

Cada persona lidera un área (decide y revisa los PRs de esa área) y todas abren al menos un PR.

| Nombre | Lidera | Tareas | GitHub |
| --- | --- | --- | --- |
| [Nombre] | [Diseño / Frontend / Backend y datos / Pruebas / Despliegue / Docs y pitch] | [T1, T4] | [@usuario] |
| [Nombre] | [ ] | [ ] | [@usuario] |
| [Nombre] | [ ] | [ ] | [@usuario] |
| [Nombre] | [ ] | [ ] | [@usuario] |

## Cómo trabajamos

- `main` siempre funciona, y todo entra por pull request revisado por una compañera.
- Una tarea = un issue = una rama. El tablero dice quién hace qué.
- La IA propone, una persona decide.

Reglas completas: [CONTRIBUTING.md](CONTRIBUTING.md) para personas y [AGENTS.md](AGENTS.md) para la IA. El flujo, en [docs/FLUJO-SDD.md](docs/FLUJO-SDD.md).

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

Hecho en la Warmi Innovathon 2026, con el apoyo de Ubuntu, Makipuray, Microsoft y GitHub Education. Créditos de las skills en [NOTICE.md](NOTICE.md).
