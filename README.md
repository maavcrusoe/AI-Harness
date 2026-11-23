# Herramientas, plugins, skills y recursos para agentes de IA

> [!IMPORTANT]
> **Aviso informativo y educativo.** Este documento es un recap de herramientas, plugins, skills y recursos que se pueden usar con agentes de IA. No constituye una recomendación, garantía ni auditoría de seguridad. Se actualiza periódicamente y la disponibilidad, compatibilidad y comportamiento de cada proyecto pueden cambiar. Antes de instalar o ejecutar cualquier componente, revisa su código, licencia, hooks, MCP, scripts, permisos y tratamiento de datos; en empresa, fija versiones o commits y prueba primero en un perfil aislado.

**Leyenda de etiquetas:** 🟥 **solapamiento alto / no apilar** · 🟧 **solapamiento parcial / probar por separado** · 🟩 **compatible o complementario** · 🟦 **base o referencia preferente**.

---

## 📑 Índice navegable

- [1. 🧠 Optimización de contexto, tokens y memoria](#1-optimizacion-de-contexto-tokens-y-memoria)
  - [Caveman](#caveman)
  - [Headroom](#headroom)
  - [Claude-Mem](#claude-mem)
  - [Compactación automática](#compactacion-automatica)
  - [Token Reducer](#token-reducer)
  - [cctx: Claude Code Token Optimizer](#cctx-claude-code-token-optimizer)
  - [Context Mode — recomendado](#context-mode-recomendado)
- [2. 🎨 Skills de diseño, frontend y contenido](#2-skills-de-diseno-frontend-y-contenido)
  - [Taste Skill](#taste-skill)
  - [Impeccable](#impeccable)
  - [Hallmark](#hallmark)
  - [Humanizer](#humanizer)
  - [Marketing Skills](#marketing-skills)
  - [SkillUI](#skillui)
  - [UI UX Pro Max](#ui-ux-pro-max)
  - [Awesome DESIGN.md](#awesome-designmd)
  - [img2threejs](#img2threejs)
  - [Impeccable, instalación y comandos actuales](#impeccable-instalacion-y-comandos-actuales)
- [3. 🧑‍💻 Desarrollo controlado y revisión de código](#3-desarrollo-controlado-y-revision-de-codigo)
  - [Superpowers](#superpowers)
  - [OpenAI Codex Plugin para Claude Code](#openai-codex-plugin-para-claude-code)
  - [SDD Skills: Agent Skills de Addy Osmani](#sdd-skills-agent-skills-de-addy-osmani)
  - [Matt Pocock Skills](#matt-pocock-skills)
  - [Karpathy Guidelines](#karpathy-guidelines)
  - [One Skill to Rule Them All / Task Observer](#one-skill-to-rule-them-all-task-observer)
  - [I Have ADHD](#i-have-adhd)
  - [Prompt Audit / Anukkrit Skills](#prompt-audit-anukkrit-skills)
- [4. 🔐 Seguridad de código, skills y agentes](#4-seguridad-de-codigo-skills-y-agentes)
  - [Cloudflare Security Audit Skill — muy recomendado](#cloudflare-security-audit-skill-muy-recomendado)
  - [NVIDIA SkillSpector — recomendado](#nvidia-skillspector-recomendado)
  - [Anthropic Cybersecurity Skills](#anthropic-cybersecurity-skills)
- [5. 🌐 Investigación, web y proveedores](#5-investigacion-web-y-proveedores)
  - [Last30Days](#last30days)
  - [Agent Reach](#agent-reach)
  - [OmniRoute](#omniroute)
- [6. 🗺️ Mapas de conocimiento y arquitectura](#6-mapas-de-conocimiento-y-arquitectura)
  - [Graphify](#graphify)
  - [CodeGraph](#codegraph)
  - [Archify](#archify)
  - [Diagram Design](#diagram-design)
- [7. 🎬 Vídeo y voz](#7-video-y-voz)
  - [HyperFrames](#hyperframes)
  - [Brag](#brag)
  - [Voicebox](#voicebox)
  - [Prompt Motion](#prompt-motion)
- [8. 🤖 Plugins, mods y subagentes](#8-plugins-mods-y-subagentes)
  - [Mission Control](#mission-control)
  - [Ponytail](#ponytail)
  - [Savvy Flow](#savvy-flow)
  - [Savvy Progress](#savvy-progress)
- [9. 🛠️ Gestión, pruebas, especificaciones y métricas](#9-gestion-pruebas-especificaciones-y-metricas)
  - [Claude Code Setup](#claude-code-setup)
  - [Claude Code Tool Manager — guardado, no probado](#claude-code-tool-manager-guardado-no-probado)
  - [Playwright MCP](#playwright-mcp)
  - [OpenSpec](#openspec)
  - [OpenMeter](#openmeter)
  - [Super Board](#super-board)
  - [Software Factory for Claude Code v2 — ZazenCodes](#software-factory-for-claude-code-v2-zazencodes)
  - [AI Software Factory — Piomin](#ai-software-factory-piomin)
  - [Orden recomendado para evaluar una factoría](#orden-recomendado-para-evaluar-una-factoria)
- [10. 🗃️ Obsidian y segundo cerebro](#10-obsidian-y-segundo-cerebro)
  - [Claudian](#claudian)
  - [Claude Obsidian](#claude-obsidian)
  - [Obsidian Second Brain](#obsidian-second-brain)
  - [Obsidian AI Second Brain](#obsidian-ai-second-brain)
  - [LLM Wiki Second Brain](#llm-wiki-second-brain)
- [11. 🔎 Webs y catálogos útiles](#11-webs-y-catalogos-utiles)
  - [AI Templates](#ai-templates)
  - [Biblioteca de prompts — prompts.chat](#biblioteca-de-prompts--promptschat)
  - [Can I run AI locally?](#can-i-run-ai-locally)
  - [The Agent Skills Directory — Skills.sh](#the-agent-skills-directory--skillssh)
  - [Modelos — LocalMaxxing](#modelos--localmaxxing)
  - [Claude Code Plugins — Claude Marketplaces](#claude-code-plugins--claude-marketplaces)
  - [better-claude](#better-claude)
  - [Spark Plug](#spark-plug)
  - [AGENTS.md](#agentsmd)
- [🎯 Variables prioritarias](#variables-prioritarias)
- [✅ Recomendaciones finales](#recomendaciones-finales)

> Las imágenes son clicables y proceden del propio repositorio cuando existe un activo identificable. En los demás artículos se mantiene la vista social oficial de GitHub como respaldo.

---
## 1. 🧠 Optimización de contexto, tokens y memoria

### Caveman

**Repositorio:** https://github.com/JuliusBrussee/caveman
[![Vista de Caveman](https://opengraph.githubassets.com/1/JuliusBrussee/caveman)](https://github.com/JuliusBrussee/caveman)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Skill y proxy local para acortar respuestas y comprimir salidas de herramientas, manteniendo la posibilidad de recuperar el contenido original. Compatible con Claude Code, Codex, Cursor y otros agentes.

**Etiquetas:** 🟥 **Solapa con:** Context Mode y RTK · 🟧 **Precaución:** modifica deliberadamente el estilo de respuesta hacia una comunicación ultrabreve · 🟩 **Mejor encaje:** usarlo como modo alternativo aislado cuando prima la brevedad, no apilado con otros reductores.

**Instalación en Windows PowerShell, versión 4.1.0:**

```powershell
npx @caveman-ai/cli@latest
claude plugin marketplace add JuliusBrussee/caveman && claude plugin install caveman@caveman
```

**Comprobación y estadísticas:**

```powershell
caveman --help
caveman stats
```

---
### Headroom

**Repositorio:** https://github.com/headroomlabs-ai/headroom
[![Vista de Headroom](https://raw.githubusercontent.com/headroomlabs-ai/headroom/main/HeadroomDemo-Fast.gif)](https://github.com/headroomlabs-ai/headroom)

<sub>Imagen: activo incluido en el repositorio. Haz clic para abrir el repositorio.</sub>

Proxy, librería y servidor MCP que comprime logs, archivos, JSON, resultados de herramientas y fragmentos RAG antes de enviarlos al modelo.

**Instalación:**

```bash
uv tool install "headroom-ai[proxy]"
headroom init claude
```

**Comprobación:**

```bash
headroom --version
headroom stats
```

`headroom stats` permite revisar solicitudes, compresión y ahorro aproximado de tokens.

---
### Claude-Mem

**Repositorio:** https://github.com/thedotmack/claude-mem
[![Vista de Claude-Mem](https://opengraph.githubassets.com/1/thedotmack/claude-mem)](https://github.com/thedotmack/claude-mem)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Memoria persistente local entre sesiones. Captura la actividad del agente, la resume y recupera contexto relevante en sesiones posteriores. Puede escanear e importar sesiones anteriores, según las funciones disponibles en la versión instalada.

Está orientado principalmente al espacio de trabajo de una persona. No debe tratarse como memoria compartida de equipo sin añadir sincronización, control de acceso, revisión, retención y filtrado de secretos.

**Instalación rápida:**

```bash
npx claude-mem install
```

**Instalación como plugin de Claude Code:**

```text
/plugin marketplace add thedotmack/claude-mem
/plugin install claude-mem
```

Reinicia Claude Code. Antes de usarlo con repositorios empresariales, revisa qué datos captura, dónde los guarda y cómo excluye secretos.


---
### Compactación automática

No desactives la compactación automática en sesiones de trabajo normales. Evita configurar:

```text
DISABLE_AUTO_COMPACT=1
DISABLE_COMPACT=1
```

Base recomendada:

```json
{
  "env": {
    "CLAUDE_CODE_TRANSCRIPT_LOCAL_GC": "1",
    "CLAUDE_CODE_PROMPT_CACHE_TTL": "1h",
    "CLAUDE_CODE_SUBAGENT_PROMPT_CACHE_TTL": "1h"
  }
}
```

La anotación “auto compact 600k” no corresponde a una variable universal. Si un gateway presenta un modelo personalizado cuya ventana no reconoce Claude Code, configura `CLAUDE_CODE_MAX_CONTEXT_TOKENS` con la capacidad real del modelo.

---


### Token Reducer

**Repositorio:** https://github.com/Madhan230205/token-reducer
[![Vista de Token Reducer](https://opengraph.githubassets.com/1/Madhan230205/token-reducer)](https://github.com/Madhan230205/token-reducer)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Plugin local-first para recuperar únicamente el contexto relevante mediante BM25, vectores, AST, reranking y compresión. El repositorio declara reducciones del 90-98 % en sus benchmarks; deben validarse con cargas reales antes de adoptar esas cifras.

**Etiquetas:** 🟥 **Solapa con:** Context Mode y RTK · 🟩 **Mejor encaje:** proyectos de código donde se necesite recuperación híbrida BM25 + vectores + AST; úsalo como capa principal de recuperación, no junto a otra equivalente.

**Instalación como plugin:**

```text
/plugin marketplace add Madhan230205/token-reducer
/plugin install token-reducer@Madhan230205-token-reducer
```

**Instalación por proyecto:**

```text
/plugin install token-reducer@Madhan230205-token-reducer --scope project
```

---
### cctx: Claude Code Token Optimizer

**Repositorio:** https://github.com/anil7948/cctx#cctx--claude-code-token-optimizer
[![Vista de cctx: Claude Code Token Optimizer](https://opengraph.githubassets.com/1/anil7948/cctx)](https://github.com/anil7948/cctx)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

CLI, MCP y Stop hook que utiliza un modelo local mediante Ollama para indexar el proyecto, comprimir salidas de herramientas, resumir turnos y mantener memoria entre sesiones.

**Etiquetas:** 🟥 **Solapa con:** Context Mode y RTK · 🟩 **Mejor encaje:** entornos con Ollama local que quieran indexación, compresión y memoria en una sola capa; evita combinar sus hooks con otros optimizadores de contexto.

**Requisitos:** Node.js 20+, aproximadamente 2,5 GB de disco para el modelo predeterminado y Claude Code. En Windows se recomienda WSL.

```bash
npm install -g cctx-optimizer
cctx setup
cctx doctor
cctx index run
cctx session stats
```

---
### Context Mode — recomendado

**Repositorio:** https://github.com/mksglu/context-mode
[![Vista de Context Mode — recomendado](https://opengraph.githubassets.com/1/mksglu/context-mode)](https://github.com/mksglu/context-mode)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Plugin local que mantiene la salida completa de herramientas fuera del contexto del agente, la almacena en SQLite FTS5 y devuelve solo los fragmentos necesarios. Funciona con Claude Code, Codex, Gemini CLI, OpenCode, Copilot CLI y otros agentes. Tiene telemetría desactivada y conserva los índices localmente.

**Etiquetas:** 🟦 **Base preferente:** reducción de contexto sin otro LLM local · 🟥 **Alternativas solapadas:** Caveman, Token Reducer, cctx y RTK; selecciona una sola capa principal y compara resultados.

**Requisitos:** Node.js 24.15 o superior. En Windows requiere Git for Windows.

**Instalación en Claude Code:**

```bash
claude plugin marketplace add mksglu/context-mode
claude plugin install context-mode@context-mode
claude plugin list
```

**Valoración:** recomendado como primera opción para reducir el crecimiento del contexto sin incorporar otro LLM local. Antes de combinarlo con Caveman, Headroom, Token Reducer o cctx, prueba cada herramienta por separado para evitar hooks duplicados y compresión excesiva.

---

[⬆️ Volver al índice](#indice-navegable)

## 2. 🎨 Skills de diseño, frontend y contenido
### Taste Skill

**Repositorio:** https://github.com/Leonxlnx/taste-skill
[![Vista de Taste Skill](https://opengraph.githubassets.com/1/Leonxlnx/taste-skill)](https://github.com/Leonxlnx/taste-skill)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Skill de dirección de arte y frontend para evitar páginas genéricas generadas por IA. Utiliza sistemas de diseño, referencias visuales, fotografías, movimiento y comprobación en navegador.

**Etiquetas:** 🟥 **Solapa con:** Frontend Design, Hallmark e Impeccable · 🟩 **Compatible con:** SkillUI o Awesome DESIGN.md como fuente previa del sistema visual.

```bash
npx skills add https://github.com/Leonxlnx/taste-skill --skill "design-taste-frontend"
```

Uso sugerido:

```text
Usa design-taste-frontend para rediseñar esta página y comprobarla en un navegador.
```

---
### Impeccable

**Repositorio:** https://github.com/pbakaus/impeccable
[![Vista de Impeccable](https://opengraph.githubassets.com/1/pbakaus/impeccable)](https://github.com/pbakaus/impeccable)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Sistema para crear, revisar, auditar y pulir interfaces. Incluye controles de tipografía, color, movimiento, responsive, accesibilidad y patrones visuales generados por IA.

```bash
npx skills add pbakaus/impeccable -g
```

Ejemplos, según la versión instalada:

```text
/impeccable audit src/pages
/impeccable critique
/impeccable polish
/impeccable animate
/impeccable harden
```

---
### Hallmark

**Repositorio:** https://github.com/Nutlope/hallmark
[![Vista de Hallmark](https://raw.githubusercontent.com/Nutlope/hallmark/main/docs/screenshots/refract.png)](https://github.com/Nutlope/hallmark)

<sub>Imagen: activo incluido en el repositorio. Haz clic para abrir el repositorio.</sub>

Skill de diseño anti-AI-slop para Claude Code, Codex, Cursor y OpenCode. Revisa contraste, foco, movimiento, responsive, formularios y patrones visuales repetitivos.

**Etiquetas:** 🟥 **Solapa con:** Frontend Design, Taste Skill e Impeccable · 🟩 **Compatible con:** SkillUI para auditar una interfaz a partir de un sistema visual ya extraído.

```bash
npx skills add Nutlope/hallmark -g
```

Uso:

```text
Usa Hallmark para rediseñar y auditar esta interfaz.
```

---
### Humanizer

**Repositorio:** https://github.com/blader/humanizer
[![Vista de Humanizer](https://opengraph.githubassets.com/1/blader/humanizer)](https://github.com/blader/humanizer)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Elimina patrones habituales de escritura generada por IA sin cambiar el significado. No está diseñado para evadir detectores.

**Etiquetas:** 🟧 **Solapamiento parcial:** Frontend Design y skills anti-slop cuando también revisan microcopy · 🟩 **Compatible con:** Marketing Skills para pulir texto después de definir estrategia, intención y tono.

```bash
npx skills add blader/humanizer -g
```

```text
/humanizer
```

---
### Marketing Skills

**Repositorio recomendado:** https://github.com/coreyhaines31/marketing-skills
[![Vista de Marketing Skills](https://opengraph.githubassets.com/1/coreyhaines31/marketing-skills)](https://github.com/coreyhaines31/marketing-skills)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Colección de skills de CRO, copywriting, SEO, analítica, experimentación, contenido y crecimiento.

```bash
npx skills add coreyhaines31/marketing-skills -g
```

Ejemplos:

```text
Usa page-cro para auditar esta landing page.
Usa analytics-tracking para diseñar el plan de medición.
Usa content-strategy para crear una estrategia trimestral.
Usa ab-test-setup para diseñar un experimento.
```

---

### SkillUI

**Repositorio:** https://github.com/amaancoderx/npxskillui
[![Vista de SkillUI](https://raw.githubusercontent.com/amaancoderx/npxskillui/main/skillui.png)](https://github.com/amaancoderx/npxskillui)

<sub>Imagen: activo incluido en el repositorio. Haz clic para abrir el repositorio.</sub>

CLI sin API ni modelo de IA que extrae el sistema visual de una URL, un repositorio o un proyecto local. Genera `DESIGN.md`, `SKILL.md`, `CLAUDE.md`, tokens, fuentes y, en modo Ultra, capturas y análisis de interacciones mediante Playwright.

**Instalación:**

```bash
npm install -g skillui
```

Requiere Node.js 18 o superior. Para el modo Ultra:

```bash
npm install playwright
npx playwright install chromium
```

**Uso:**

```bash
skillui --url https://linear.app
skillui --url https://linear.app --mode ultra --screens 10
skillui --dir ./mi-app
skillui --repo https://github.com/organizacion/repositorio
```

---
### UI UX Pro Max

**Repositorio:** https://github.com/nextlevelbuilder/ui-ux-pro-max-skill
[![Vista de UI UX Pro Max](https://raw.githubusercontent.com/nextlevelbuilder/ui-ux-pro-max-skill/main/screenshots/website.png)](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)

<sub>Imagen: activo incluido en el repositorio. Haz clic para abrir el repositorio.</sub>

Skill de inteligencia de diseño para generar sistemas UI/UX adaptados al sector, producto y stack. Incluye estilos visuales, paletas, tipografías, patrones de landing, gráficos, reglas responsive y comprobaciones de accesibilidad.

**Etiquetas:** 🟥 **Solapa con:** Frontend Design, Taste Skill, Hallmark e Impeccable · 🟩 **Compatible con:** SkillUI y Awesome DESIGN.md cuando se use como capa de recomendaciones sobre un sistema visual concreto.

**Instalación recomendada:**

```bash
npx skills add nextlevelbuilder/ui-ux-pro-max-skill -g
```

También admite integración como plugin de Claude Code según el método publicado en el repositorio.

**Uso:**

```text
Usa UI UX Pro Max para diseñar un dashboard empresarial responsive y accesible.
```

---
### Awesome DESIGN.md

**Repositorio principal:** https://github.com/VoltAgent/awesome-design-md
[![Vista de Awesome DESIGN.md](https://opengraph.githubassets.com/1/VoltAgent/awesome-design-md)](https://github.com/VoltAgent/awesome-design-md)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Colección de archivos `DESIGN.md` inspirados en sistemas visuales de productos conocidos. Se copia el estilo elegido en la raíz del proyecto para que el agente mantenga una dirección visual consistente.

**Alternativa en formato Agent Skill:** https://github.com/bergside/awesome-design-skills

Ejemplo de instalación de un estilo mediante TypeUI:

```bash
npx typeui.sh pull enterprise
npx typeui.sh pull minimal
npx typeui.sh pull impeccable
```

---
### img2threejs

**Repositorio:** https://github.com/img2threejs/img2threejs
[![Vista de img2threejs](https://opengraph.githubassets.com/1/img2threejs/img2threejs)](https://github.com/img2threejs/img2threejs)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Reconstruye el objeto de una imagen de referencia como un modelo procedural de Three.js, generado completamente mediante código, preparado para animación y sometido a comprobaciones de calidad. No es fotogrametría ni descarga modelos externos.

**Uso recomendado:** seguir el instalador de la release del repositorio y proporcionar al agente una imagen de referencia. Es apropiado para objetos, props y elementos de escenas web 3D.

**Complemento para escenas y gráficos Three.js:** https://github.com/scottstts/Threejs-Awesome-Graphics-Agent-Skills

---
### Impeccable, instalación y comandos actuales

**Web de descarga:** https://impeccable.style/#downloads

Skill de diseño que detecta y elimina patrones visuales de baja calidad o “AI slop”. Añade vocabulario de diseño y comandos para mejorar jerarquía, claridad, densidad, tipografía y coherencia.

**Instalación:**

```bash
npx impeccable install
```

**Comandos destacados:**

```text
/polish
/distill
/clarify
```

`/polish` refina la ejecución visual, `/distill` simplifica interfaces cargadas y `/clarify` mejora la claridad del contenido y la jerarquía.

---

[⬆️ Volver al índice](#indice-navegable)

## 3. 🧑‍💻 Desarrollo controlado y revisión de código

### Superpowers

**Repositorio:** https://github.com/obra/superpowers
[![Vista de Superpowers](https://opengraph.githubassets.com/1/obra/superpowers)](https://github.com/obra/superpowers)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Framework de skills para brainstorming, planificación, TDD, depuración sistemática, revisión, ejecución por fases y agentes paralelos.

```text
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
/reload-plugins
```

Uso habitual:

```text
/brainstorm
/write-plan
/execute-plan
```

---
### OpenAI Codex Plugin para Claude Code

**Repositorio oficial:** https://github.com/openai/codex-plugin-cc
[![Vista de OpenAI Codex Plugin para Claude Code](https://opengraph.githubassets.com/1/openai/codex-plugin-cc)](https://github.com/openai/codex-plugin-cc)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Permite ejecutar Codex desde Claude Code para revisar cambios, realizar revisiones adversariales y delegar tareas en segundo plano.

**Requisitos:** Node.js 18.18 o superior y acceso a Codex mediante una suscripción compatible o API key.

```text
/plugin marketplace add openai/codex-plugin-cc
/plugin install codex@openai-codex
/reload-plugins
/codex:setup
```

Si falta Codex CLI:

```bash
npm install -g @openai/codex
codex login
```

Comandos:

```text
/codex:review --background
/codex:adversarial-review
/codex:status
/codex:result
/codex:cancel
/codex:transfer
/codex:rescue
```

---
### SDD Skills: Agent Skills de Addy Osmani

**Repositorio recomendado:** https://github.com/addyosmani/agent-skills
[![Vista de SDD Skills: Agent Skills de Addy Osmani](https://opengraph.githubassets.com/1/addyosmani/agent-skills)](https://github.com/addyosmani/agent-skills)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Colección de skills de ingeniería para un ciclo completo de desarrollo guiado por especificaciones: definición, planificación, implementación incremental, pruebas, restricciones de calidad, revisión, rendimiento web, accesibilidad, simplificación y entrega.

**Instalación con Skills CLI:**

```bash
npx skills add addyosmani/agent-skills
```

**Instalación como plugin de Claude Code:**

```text
/plugin marketplace add addyosmani/agent-skills
/plugin install agent-skills@addy-agent-skills
```

**Flujo:**

```text
/spec
/plan
/build
/test
/constraints
/review
/webperf
/a11y
/code-simplify
/ship
```

> Nota: el comando documentado por el repositorio es `/a11y`, no `/ally`. Si un comando entra en conflicto con uno nativo de Claude Code, utiliza la forma namespaced, por ejemplo `/agent-skills:review`.

---
### Matt Pocock Skills

**Repositorio:** https://github.com/mattpocock/skills
[![Vista de Matt Pocock Skills](https://opengraph.githubassets.com/1/mattpocock/skills)](https://github.com/mattpocock/skills)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Colección de skills pequeñas y combinables para ingeniería de software.

```bash
npx skills@latest add mattpocock/skills
```

Selecciona también `setup-matt-pocock-skills` y ejecútala:

```text
/setup-matt-pocock-skills
```

---
### Karpathy Guidelines

**Repositorio:** https://github.com/multica-ai/andrej-karpathy-skills
[![Vista de Karpathy Guidelines](https://opengraph.githubassets.com/1/multica-ai/andrej-karpathy-skills)](https://github.com/multica-ai/andrej-karpathy-skills)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Reglas inspiradas en observaciones de Andrej Karpathy: pensar antes de programar, reducir complejidad, hacer cambios quirúrgicos y trabajar con criterios verificables.

```bash
npx skills add multica-ai/andrej-karpathy-skills -g
```

---

### One Skill to Rule Them All / Task Observer

**Repositorio:** https://github.com/rebelytics/one-skill-to-rule-them-all
[![Vista de One Skill to Rule Them All / Task Observer](https://opengraph.githubassets.com/1/rebelytics/one-skill-to-rule-them-all)](https://github.com/rebelytics/one-skill-to-rule-them-all)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Meta-skill que observa correcciones, decisiones y trabajos repetitivos para proponer mejoras a las skills existentes o nuevas skills candidatas. También evalúa su propio funcionamiento. No modifica las skills activas directamente: registra evidencias y prepara propuestas para revisión humana.

**Instalación:**

```bash
npx skills@1.8.1 add rebelytics/one-skill-to-rule-them-all --skill task-observer
```

Para todos los proyectos:

```bash
npx skills@1.8.1 add rebelytics/one-skill-to-rule-them-all --skill task-observer -g
```

**Como plugin de Claude Code:**

```text
/plugin marketplace add rebelytics/one-skill-to-rule-them-all
/plugin install task-observer@one-skill-to-rule-them-all
/reload-plugins
```

**Importante:** instalarla no garantiza que se active. Añade el hook de inicio y el bloque de activación de `references/environments.md` al `CLAUDE.md`. Comprueba en una sesión nueva que se crea `skill-observations/observation-log/`.


---
### I Have ADHD

**Repositorio:** https://github.com/ayghri/i-have-adhd
[![Vista de I Have ADHD](https://raw.githubusercontent.com/ayghri/i-have-adhd/main/logo.png)](https://github.com/ayghri/i-have-adhd)

<sub>Imagen: activo incluido en el repositorio. Haz clic para abrir el repositorio.</sub>

Skill de estilo de respuesta que fuerza al agente a poner primero la acción, numerar pasos, eliminar tangentes y cerrar con un siguiente paso concreto. Puede utilizarse para lograr respuestas más directas aunque el usuario no tenga TDAH.

**Instalación:**

```bash
claude plugin marketplace add ayghri/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

**Ejecución:**

```text
/i-have-adhd
```

Evita preámbulos, limita las listas y elimina cierres vacíos como “Espero que te ayude”.


---
### Prompt Audit / Anukkrit Skills

**Repositorio:** https://github.com/anukkrit149/anukkrit-skills
[![Vista de Prompt Audit / Anukkrit Skills](https://opengraph.githubassets.com/1/anukkrit149/anukkrit-skills)](https://github.com/anukkrit149/anukkrit-skills)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Marketplace con skills de documentación, investigación, planificación, prompts, datos, frontend y desarrollo.

Comando anotado originalmente:

```bash
npx skillfish add anukkrit149/anukkrit-skills prompt-audit
```

Método mediante marketplace:

```text
/plugin marketplace add git@github.com:anukkrit149/anukkrit-skills.git
/plugin install anukkrit-skills-cloud@anukkrit-skills
```

Para Cowork:

```text
/plugin install anukkrit-skills-cowork@anukkrit-skills
```

Comprueba `/help` para confirmar el nombre actual de `prompt-audit`.

---


[⬆️ Volver al índice](#indice-navegable)

## 4. 🔐 Seguridad de código, skills y agentes
### Cloudflare Security Audit Skill — muy recomendado

**Repositorio:** https://github.com/cloudflare/security-audit-skill
[![Vista de Cloudflare Security Audit Skill — muy recomendado](https://opengraph.githubassets.com/1/cloudflare/security-audit-skill)](https://github.com/cloudflare/security-audit-skill)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Skill de auditoría de seguridad en seis fases: reconocimiento, cobertura, búsqueda aislada, validación independiente, resultados estructurados y generación de informes. Produce `findings.json`, `REPORT.md`, un ledger de cobertura y separa resultados confirmados, pendientes de validación y rechazados.

```bash
npx skills add https://github.com/cloudflare/security-audit-skill --skill security-audit --global
```

**Uso:**

```text
security audit this codebase
find security vulnerabilities in ./src
do a security review, output to ~/audits/my-project
```

**Valoración:** muy recomendado para revisiones defensivas. Los builds y pruebas de código no confiable deben ejecutarse en un sandbox sin red, con variables permitidas, límites de recursos y rutas de escritura restringidas.

---
### NVIDIA SkillSpector — recomendado

**Repositorio:** https://github.com/NVIDIA/skillspector
[![Vista de NVIDIA SkillSpector — recomendado](https://opengraph.githubassets.com/1/NVIDIA/skillspector)](https://github.com/NVIDIA/skillspector)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Escáner de seguridad para skills antes de instalarlas. Analiza inyección de prompts, exfiltración, escalada de privilegios, supply chain, MCP, código peligroso y otros patrones. Genera informes de terminal, JSON, Markdown y SARIF con puntuación de riesgo.

**Instalación:**

```bash
uv tool install git+https://github.com/NVIDIA/skillspector.git
```

Con soporte MCP:

```bash
uv tool install 'skillspector[mcp] @ git+https://github.com/NVIDIA/skillspector.git'
```

**Uso recomendado antes de instalar cualquier skill externa:**

```bash
skillspector scan https://github.com/usuario/skill --no-llm
skillspector scan ./skill-local --format sarif --output skillspector.sarif
```

**Valoración:** recomendado como puerta de entrada en CI o en un proceso de aprobación empresarial.

---
### Anthropic Cybersecurity Skills

**Repositorio comunitario:** https://github.com/mukul975/Anthropic-Cybersecurity-Skills
[![Vista de Anthropic Cybersecurity Skills](https://opengraph.githubassets.com/1/mukul975/Anthropic-Cybersecurity-Skills)](https://github.com/mukul975/Anthropic-Cybersecurity-Skills)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Biblioteca comunitaria, no afiliada a Anthropic, con skills de seguridad mapeadas a MITRE ATT&CK, NIST CSF 2.0, MITRE ATLAS, D3FEND, NIST AI RMF y MITRE F3. Incluye contenidos defensivos y de doble uso.

```bash
npx skills add mukul975/Anthropic-Cybersecurity-Skills
```

Utilízala únicamente sobre sistemas propios o con autorización escrita y selecciona solo los dominios necesarios para no sobrecargar el agente.

---

[⬆️ Volver al índice](#indice-navegable)

## 5. 🌐 Investigación, web y proveedores
### Last30Days

**Repositorio:** https://github.com/mvanhorn/last30days-skill
[![Vista de Last30Days](https://opengraph.githubassets.com/1/mvanhorn/last30days-skill)](https://github.com/mvanhorn/last30days-skill)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Investiga un tema usando información publicada durante los últimos 30 días en Reddit, X, YouTube, Hacker News, Polymarket y la web. No analiza tu uso personal de Claude.

```bash
npx skills add mvanhorn/last30days-skill -g
```

Como plugin:

```text
/plugin marketplace add mvanhorn/last30days-skill
/plugin install last30days
```

Uso:

```text
/last30days agentes de programación con memoria persistente
```

---
### Agent Reach

**Repositorio principal:** https://github.com/Panniantong/Agent-Reach
[![Vista de Agent Reach](https://opengraph.githubassets.com/1/Panniantong/Agent-Reach)](https://github.com/Panniantong/Agent-Reach)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Proporciona lectura y búsqueda sobre web, YouTube, Reddit, X, GitHub, RSS y otras plataformas.

```bash
npx skills add Panniantong/Agent-Reach@agent-reach
```

Instalación manual:

```bash
pip install https://github.com/Panniantong/agent-reach/archive/main.zip
agent-reach install --env=auto
agent-reach doctor
```

`agent-reach doctor` muestra qué integraciones funcionan y qué configuración falta.

---
### OmniRoute

**Repositorio:** https://github.com/cheaper-inference/OmniRoute
[![Vista de OmniRoute](https://raw.githubusercontent.com/diegosouzapw/OmniRoute/HEAD/docs/screenshots/MainOmniRoute.png)](https://github.com/cheaper-inference/OmniRoute)

<sub>Imagen: activo incluido en el repositorio. Haz clic para abrir el repositorio.</sub>

Gateway MIT con interfaz visual que unifica proveedores y modelos bajo un endpoint compatible. Permite administrar credenciales, cuotas, rutas y fallback cuando un proveedor, una credencial o un modelo deja de estar disponible.

No amplía la ventana de contexto de un modelo. Puede cambiar a otra ruta cuando se agota una cuota o falla un proveedor, pero la continuidad depende de que el modelo de destino admita el contexto y las capacidades utilizadas.

**Endpoint habitual:**

```text
http://localhost:20128
```

**Ejemplo para Claude Code:**

```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "http://127.0.0.1:20128",
    "ANTHROPIC_MODEL": "auto"
  }
}
```

Los tiers gratuitos requieren cuentas propias cuando corresponda y están sujetos a cuotas, regiones y condiciones de cada proveedor.


---

[⬆️ Volver al índice](#indice-navegable)

## 6. 🗺️ Mapas de conocimiento y arquitectura
### Graphify

**Repositorio:** https://github.com/Graphify-Labs/graphify
[![Vista de Graphify](https://opengraph.githubassets.com/1/Graphify-Labs/graphify)](https://github.com/Graphify-Labs/graphify)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Convierte código, documentación, SQL y otros archivos en un grafo de conocimiento consultable. Para el código utiliza AST y distingue relaciones extraídas de relaciones inferidas.

**Etiquetas:** 🟥 **Solapa con:** CodeGraph cuando ambos indexan el mismo código · 🟩 **Compatible con CodeGraph:** solo si se separa el alcance, por ejemplo CodeGraph para código vivo y Graphify para documentación, SQL u otras fuentes.

```bash
npx skills add Graphify-Labs/graphify -g
```

```text
/graphify
```

---
### CodeGraph

**Repositorio:** https://github.com/colbymchenry/codegraph
[![Vista de CodeGraph](https://opengraph.githubassets.com/1/colbymchenry/codegraph)](https://github.com/colbymchenry/codegraph)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Grafo de código local, preindexado y sincronizado con los cambios del repositorio.

**Etiquetas:** 🟦 **Base preferente para código:** indexación local sincronizada · 🟩 **Compatible con:** Archify o Diagram Design como capa posterior de visualización; con Graphify, separa las fuentes para evitar doble indexación.

**Windows PowerShell:**

```powershell
irm https://raw.githubusercontent.com/colbymchenry/codegraph/main/install.ps1 | iex
```

**npm:**

```bash
npm install -g @colbymchenry/codegraph
```

```bash
codegraph --help
codegraph upgrade
```

---
### Archify

**Repositorio:** https://github.com/tt-a1i/archify
[![Vista de Archify](https://opengraph.githubassets.com/1/tt-a1i/archify)](https://github.com/tt-a1i/archify)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Convierte una descripción, plan o codebase en un diagrama HTML interactivo.

**Etiquetas:** 🟧 **Solapamiento parcial con:** CodeGraph en exploración de arquitectura · 🟩 **Compatible con CodeGraph:** úsalo como salida visual interactiva, dejando a CodeGraph la indexación y consulta del código.

```bash
npx skills add tt-a1i/archify -g
```

Uso:

```text
Usa Archify para diagramar navegador -> API -> Redis -> PostgreSQL.
```

---

[⬆️ Volver al índice](#indice-navegable)


### Diagram Design

**Repositorio:** https://github.com/cathrynlavery/diagram-design

[![Logo de Diagram Design](https://raw.githubusercontent.com/cathrynlavery/diagram-design/main/assets/logo.png)](https://github.com/cathrynlavery/diagram-design)

<sub>Imagen incluida en el repositorio. Haz clic para abrir el proyecto.</sub>

Skill de diseño editorial que genera diagramas en un único archivo HTML con SVG integrado. Incluye 51 tipos de diagrama y evita depender de Mermaid. Puede adaptar paleta y tipografías a la identidad visual de un sitio, importar diagramas existentes y exportar a PNG o SVG.

**Etiquetas:** 🟧 **Solapamiento parcial con:** CodeGraph en representación de arquitectura · 🟩 **Compatible con CodeGraph:** CodeGraph aporta la estructura técnica y Diagram Design la presentación editorial y la exportación.

**Instalación compatible con varios agentes:**

```bash
npx skills add cathrynlavery/diagram-design
```

**Claude Code con marketplace y comandos slash:**

```text
/plugin marketplace add cathrynlavery/diagram-design
/plugin install diagram-design@diagram-design
```

**Ejemplos de uso:**

```text
Crea un diagrama de arquitectura de frontend, API, Redis y PostgreSQL.
Crea un diagrama de secuencia para una llamada Bearer con renovación del token al recibir un 401.
Onboard diagram-design usando la identidad visual de https://miempresa.example.
```

**Comandos disponibles en la instalación nativa, según el cliente:**

```text
/export-diagram
/import-mermaid
/import-plantuml
/profile
/doctor
```

**Recomendación:** úsalo cuando necesites diagramas presentables, editables y alineados con una marca. Para diagramas puramente técnicos y rápidos, Mermaid sigue siendo más ligero.

---

[⬆️ Volver al índice](#indice-navegable)

## 7. 🎬 Vídeo y voz
### HyperFrames

**Repositorio:** https://github.com/heygen-com/hyperframes
[![Vista de HyperFrames](https://opengraph.githubassets.com/1/heygen-com/hyperframes)](https://github.com/heygen-com/hyperframes)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Editor de vídeo abierto orientado a agentes. Genera proyectos editables y renderizables.

**Requisitos habituales:** Node.js 22 o superior, FFmpeg y Chrome/Chromium.

```bash
npx hyperframes doctor
npx hyperframes init mi-video --resolution portrait
cd mi-video
```

Para no instalar skills automáticamente:

```bash
HYPERFRAMES_SKIP_SKILLS=1 npx hyperframes init mi-video --resolution portrait
```

PowerShell:

```powershell
$env:HYPERFRAMES_SKIP_SKILLS = "1"
npx hyperframes init mi-video --resolution portrait
```

---

### Brag

**Repositorio:** https://github.com/latent-spaces/brag

[![Ejemplo de vídeo generado con Brag](https://raw.githubusercontent.com/latent-spaces/brag/main/docs/examples/horse-tinder/brag.jpg)](https://github.com/latent-spaces/brag)

<sub>Imagen incluida en la galería del repositorio. Haz clic para abrir el proyecto.</sub>

Skill que convierte un proyecto terminado en un vídeo corto de lanzamiento con música, movimiento y texto para compartir. El flujo clásico utiliza HyperFrames; `brag-slim` ofrece una variante más ligera. El resultado se guarda en `brag-output/` e incluye el plan, el brief de composición, el texto para compartir y `brag.mp4`.

**Requisitos del flujo completo:**

- Un agente compatible con Agent Skills.
- Node.js 22 o superior.
- FFmpeg disponible en `PATH`.
- HyperFrames CLI, comprobable con `npx hyperframes doctor`.

**Instalación en Claude Code:**

```text
/plugin marketplace add latent-spaces/brag
/plugin install brag@brag
```

**Instalación con Skills CLI:**

```bash
npx skills add https://github.com/latent-spaces/brag --skill brag
```

**Instalar solamente la variante ligera:**

```bash
npx skills add https://github.com/latent-spaces/brag --skill brag-slim
```

**Ejecución:**

```text
/brag
/brag --tone "lanzamiento SaaS empresarial sobrio"
/brag --voice
/brag --full
```

La narración está desactivada por defecto. `--voice` la habilita utilizando Kokoro a través de HyperFrames. En Windows, los enlaces simbólicos pueden requerir Developer Mode o una copia manual de la skill.

---

### Voicebox

**Repositorio:** https://github.com/jamiepine/voicebox
[![Vista de Voicebox](https://opengraph.githubassets.com/1/jamiepine/voicebox)](https://github.com/jamiepine/voicebox)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Estudio de voz local para clonar voces autorizadas, generar voz y dictar. Puede integrarse con agentes mediante MCP.

```bash
git clone https://github.com/jamiepine/voicebox.git
cd voicebox
docker compose up -d
```

La configuración depende de CPU, NVIDIA, AMD o Apple Silicon. Utiliza solo voces propias o con consentimiento.

---
### Prompt Motion

**Web:** https://prompt-motion.com/

Galería de motion graphics con prompts o skills reutilizables. No necesita instalación.

---

[⬆️ Volver al índice](#indice-navegable)

## 8. 🤖 Plugins, mods y subagentes

### Mission Control

**Repositorio:** https://github.com/kevin-huff/claude-code-mission-control
[![Vista de Mission Control](https://opengraph.githubassets.com/1/kevin-huff/claude-code-mission-control)](https://github.com/kevin-huff/claude-code-mission-control)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Mod para visualizar subagentes y workflows: modelo, effort, paso, duración, tokens, tareas, dependencias y previsión.

```bash
git clone https://github.com/kevin-huff/claude-code-mission-control ~/.claude/skills/mission-control
```

Reinicia Claude Code y comprueba:

```bash
claude plugin list
```

```text
/mission-control
```

Como utiliza APIs de mods en evolución, fija una versión compatible de Claude Code en empresa.

---

### Ponytail

**Repositorio oficial:** https://github.com/DietrichGebert/ponytail

[![Ponytail Board](https://raw.githubusercontent.com/DietrichGebert/ponytail/main/assets/band/board.png)](https://github.com/DietrichGebert/ponytail)

<sub>Captura `assets/band/board.png` incluida en el repositorio oficial. Haz clic para abrir el proyecto.</sub>

Skill y plugin que empuja al agente a reutilizar lo existente y escribir solo el código necesario, sin eliminar validación, seguridad, accesibilidad ni pruebas importantes. Incluye niveles `lite`, `full` y `ultra`, revisión de cambios, auditoría del repositorio, registro de deuda y un panel local de métricas.

**Instalación en Claude Code:**

```text
/plugin marketplace add DietrichGebert/ponytail
/plugin install ponytail@ponytail
```

Inicia una sesión nueva después de instalarlo. Instálalo únicamente desde `DietrichGebert/ponytail` o desde el paquete npm oficial del autor.

**Activar o cambiar el nivel:**

```text
/ponytail
/ponytail lite
/ponytail full
/ponytail ultra
/ponytail off
```

**Band y Board:**

La **band** aparece encima del prompt y muestra coste, tokens, tiempo del agente, reutilización de código y estado de las pruebas. Requiere Claude Code 2.1.290 o posterior y funciona en terminal o aplicación de escritorio; no aparece en el panel de chat de VS Code, sesiones cloud ni `claude -p`.

```text
/ponytail band on
/ponytail band off
/ponytail band import
```

`/ponytail band import` importa las sesiones anteriores de Claude Code al Board con coste, tiempo del agente y tokens. El Board reúne las tareas de todos los proyectos, sesiones, pruebas y días de actividad. Los datos se guardan localmente en:

```text
%USERPROFILE%\.config\ponytail\band\
```

En tu cuenta de Windows, el resultado esperado es:

```text
C:\Users\Miguel Angel\.config\ponytail\band\board.html
```

Y su URL local es exactamente:

```text
file:///C:/Users/Miguel%20Angel/.config/ponytail/band/board.html
```

**Cómo generar y abrir `board.html`:**

1. Instala Ponytail y abre una sesión nueva de Claude Code.
2. Activa la band:

```text
/ponytail band on
```

3. Ejecuta al menos una tarea en Claude Code para que Ponytail registre actividad.
4. Importa sesiones anteriores y actualiza el Board:

```text
/ponytail band import
```

5. Ábrelo desde PowerShell:

```powershell
$board = Join-Path $HOME '.config\ponytail\band\board.html'
if (Test-Path $board) {
    Start-Process $board
} else {
    Write-Error "No existe $board. Ejecuta /ponytail band on y /ponytail band import desde una sesión nueva de Claude Code."
}
```

También puedes pegar directamente `file:///C:/Users/Miguel%20Angel/.config/ponytail/band/board.html` en Chrome o Edge. Si el fichero todavía no existe, comprueba la versión y la instalación:

```powershell
claude --version
Get-ChildItem "$HOME\.config\ponytail\band" -Force
```

**Otros comandos útiles:**

```text
/ponytail-review
/ponytail-audit
/ponytail-debt
/ponytail-gain
/ponytail-help
```

---

### Savvy Flow

**Repositorio:** https://github.com/JohnnyVizz/claude-kit
[![Vista de Savvy Flow](https://opengraph.githubassets.com/1/JohnnyVizz/claude-kit)](https://github.com/JohnnyVizz/claude-kit)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Skill de orquestación que planifica, conserva el diseño en la sesión principal, delega en subagentes por niveles y revisa los resultados.

```text
/plugin marketplace add johnnyvizz/claude-kit
/plugin install savvy-flow@claude-kit
```

```text
/savvy-flow:savvy-flow implementar autenticación OIDC con pruebas e integración CI
```

---
### Savvy Progress

Mod complementario que añade barra de progreso y panel de subagentes con modelo, effort, contexto, coste estimado y tiempo.

```text
/plugin marketplace add johnnyvizz/claude-kit
/plugin install savvy-progress@claude-kit
```

```text
/agents-info
/agents-info open
```

El coste es una estimación, no una factura real.

---


[⬆️ Volver al índice](#indice-navegable)

## 9. 🛠️ Gestión, pruebas, especificaciones y métricas


### Claude Code Setup

**Marketplace oficial:** https://claude.com/es/marketplace/plugins/claude-code-setup

Plugin oficial que analiza el proyecto en modo de solo lectura y recomienda automatizaciones adaptadas al stack: servidores MCP, skills, hooks, subagentes y comandos. Examina la estructura, las dependencias y los patrones del repositorio.

**Ejecución:**

```text
/claude-code-setup
```

También puede invocarse con peticiones como:

```text
Recomienda automatizaciones para este proyecto.
Ayúdame a configurar Claude Code.
¿Qué hooks o servidores MCP debería usar?
```

Conviene ejecutarlo después de clonar un proyecto y repetirlo cuando cambie sustancialmente el stack.


---

### Claude Code Tool Manager — guardado, no probado

**Repositorio:** https://github.com/tylergraydev/claude-code-tool-manager
[![Vista de Claude Code Tool Manager — guardado, no probado](https://opengraph.githubassets.com/1/tylergraydev/claude-code-tool-manager)](https://github.com/tylergraydev/claude-code-tool-manager)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Aplicación de escritorio para administrar MCP, comandos, skills, subagentes, hooks, perfiles y estadísticas de varios asistentes. Sincroniza configuraciones con Claude Code, Codex, Cursor, Gemini CLI, GitHub Copilot CLI y OpenCode.

> Estado personal: **no la he probado; solo la tengo guardada para evaluarla**.

**Instalación:** descargar `.msi` o `.exe` para Windows, `.dmg` para macOS o `.AppImage`/`.deb` para Linux desde Releases. También se puede compilar con Node.js 18+, Rust 1.70+ y Tauri.

```bash
git clone https://github.com/tylergraydev/claude-code-tool-manager.git
cd claude-code-tool-manager
npm install
npm run tauri build
```

---
### Playwright MCP

**Repositorio oficial:** https://github.com/microsoft/playwright-mcp
[![Vista de Playwright MCP](https://opengraph.githubassets.com/1/microsoft/playwright-mcp)](https://github.com/microsoft/playwright-mcp)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Servidor MCP oficial de Microsoft para automatización de navegador. Permite navegación, formularios, clics, capturas, pestañas y validación de interfaces mediante snapshots de accesibilidad.

**Requisito:** Node.js 20 o superior.

**Claude Code:**

```bash
claude mcp add playwright npx @playwright/mcp@latest
```

**Configuración MCP estándar:**

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    }
  }
}
```

---
### OpenSpec

**Repositorio:** https://github.com/Fission-AI/OpenSpec
[![Vista de OpenSpec](https://opengraph.githubassets.com/1/Fission-AI/OpenSpec)](https://github.com/Fission-AI/OpenSpec)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Framework SDD para mantener propuestas, requisitos, escenarios, diseño y tareas como Markdown versionable. Está orientado tanto a proyectos nuevos como a repositorios existentes y admite planes compartidos entre varios repositorios.

**Windows PowerShell:**

```powershell
irm https://openspec.dev/cli/install.ps1 | iex
```

**npm:**

```bash
npm install -g @fission-ai/openspec@latest
cd mi-proyecto
openspec init
```

**Flujo:**

```text
/openspec-explore
/openspec-propose nombre-del-cambio
/openspec-apply-change
/openspec-archive-change
```

---
### OpenMeter

**Repositorio:** https://github.com/openmeterio/openmeter
[![Vista de OpenMeter](https://opengraph.githubassets.com/1/openmeterio/openmeter)](https://github.com/openmeterio/openmeter)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Infraestructura open source de medición y facturación por uso para IA, API y DevOps. Sirve para ingerir eventos, medir consumo, aplicar límites/créditos y alimentar facturación. No es una herramienta específica de estadísticas de Claude Code, pero puede utilizarse para medir tokens, llamadas, herramientas o coste interno si se instrumentan esos eventos.

**Quickstart local:**

```bash
git clone https://github.com/openmeterio/openmeter.git
cd openmeter/quickstart
docker compose up -d --wait
```

Úsalo si necesitas chargeback/showback por equipo, proyecto, modelo o proveedor. Para observabilidad técnica pura, OpenTelemetry y Prometheus suelen ser más sencillos.

---

### Super Board

**Repositorio:** https://github.com/EricTechPro/super-board
[![Vista de Super Board](https://opengraph.githubassets.com/1/EricTechPro/super-board)](https://github.com/EricTechPro/super-board)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Proyecto guardado como referencia de AI Factory y panel de orquestación.

**Estado:** pendiente de probar y documentar. No se incluyen comandos de instalación no verificados. Antes de utilizarlo, revisa el README, licencia, scripts, permisos, persistencia y los procesos o servicios que pone en marcha.

---
### Software Factory for Claude Code v2 — ZazenCodes

**Repositorio:** https://github.com/zazencodes/zazencodes-season-3/tree/main/src/software-factory-claude-code-v2
[![Vista de Software Factory for Claude Code v2 — ZazenCodes](https://opengraph.githubassets.com/1/zazencodes/zazencodes-season-3)](https://github.com/zazencodes/zazencodes-season-3)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Fábrica que procesa issues de GitHub etiquetados como `factory`. Los agentes hacen intake, definen alcance, escriben especificación, implementan en un worktree, ejecutan checks, revisan código, seguridad y UI, y abren una pull request. El aprobador puede fusionar cambios seguros o escalar la PR a una persona.

**Requisitos:** Claude Code 2.1.257 o superior, Python 3 y GitHub CLI `gh` autenticado con permisos para hacer push.

**Instalación asistida:**

```text
Install this software factory in this project from the reference repository:
https://github.com/zazencodes/zazencodes-season-3/tree/main/src/software-factory-claude-code-v2
```

**Ejecución:**

```text
/factory run
/factory run 123
/factory estado de los trabajos
```

**Dashboard:**

```bash
cd factory
python3 -m http.server
```

Abre `http://localhost:8000/dashboard.html`.

**Precaución:** crea ramas, hace push, abre PR y puede hacer merge. Empieza con `concurrency: 1`, revisa cada PR y protege ramas y rutas sensibles.


---
### AI Software Factory — Piomin

**Repositorio:** https://github.com/piomin/ai-software-factory
[![Vista de AI Software Factory — Piomin](https://opengraph.githubassets.com/1/piomin/ai-software-factory)](https://github.com/piomin/ai-software-factory)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Repositorio experimental con contenido bajo `openshift`. En el estado revisado no publica README, descripción ni comandos suficientes para asegurar su objetivo o instalación.

**Estado:** pendiente de revisar. Antes de desplegarlo, inspecciona sus manifiestos de OpenShift, imágenes, secretos, RBAC, almacenamiento y políticas de red.

---
### Orden recomendado para evaluar una factoría

1. Utiliza un repositorio sandbox sin secretos.
2. Configura `concurrency: 1`.
3. Protege `main` y exige checks y revisión humana.
4. Deshabilita despliegues automáticos.
5. Revisa costes, permisos de `gh`, ramas y worktrees después de cada ejecución.

---

[⬆️ Volver al índice](#indice-navegable)

## 10. 🗃️ Obsidian y segundo cerebro

### Claudian

**Repositorio:** https://github.com/YishenTu/claudian
[![Vista de Claudian](https://opengraph.githubassets.com/1/YishenTu/claudian)](https://github.com/YishenTu/claudian)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Plugin de Obsidian que integra Claude Code, Codex y otros agentes dentro del vault.

Instala la release en:

```text
VAULT/.obsidian/plugins/claudian/
```

Actívalo desde `Obsidian -> Settings -> Community plugins`.

---
### Claude Obsidian

**Repositorio:** https://github.com/AgriciDaniel/claude-obsidian
[![Vista de Claude Obsidian](https://opengraph.githubassets.com/1/AgriciDaniel/claude-obsidian)](https://github.com/AgriciDaniel/claude-obsidian)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Segundo cerebro autoorganizado para Obsidian y Claude Code. Convierte fuentes en notas Markdown enlazadas.

```text
/plugin marketplace add AgriciDaniel/claude-obsidian
/plugin install claude-obsidian
```

Comprueba los comandos instalados con `/help`.

---
### Obsidian Second Brain

**Repositorio:** https://github.com/eugeniughelbur/obsidian-second-brain
[![Vista de Obsidian Second Brain](https://opengraph.githubassets.com/1/eugeniughelbur/obsidian-second-brain)](https://github.com/eugeniughelbur/obsidian-second-brain)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Memoria persistente en Markdown para varios agentes, con búsqueda, notas autorreescribibles, investigación, tareas programadas y registro compartido.

Sigue el instalador del README y selecciona el adaptador del agente utilizado.

---
### Obsidian AI Second Brain

**Repositorio:** https://github.com/jamesmcroft/obsidian-ai-second-brain
[![Vista de Obsidian AI Second Brain](https://opengraph.githubassets.com/1/jamesmcroft/obsidian-ai-second-brain)](https://github.com/jamesmcroft/obsidian-ai-second-brain)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Plantilla CODE/PARA para Obsidian con templates, consultas y skills.

```bash
git clone https://github.com/jamesmcroft/obsidian-ai-second-brain.git
```

Abre la carpeta clonada como vault.

---
### LLM Wiki Second Brain

**Repositorio:** https://github.com/DimitrisLianos/LLM_Wiki_SecondBrain
[![Vista de LLM Wiki Second Brain](https://opengraph.githubassets.com/1/DimitrisLianos/LLM_Wiki_SecondBrain)](https://github.com/DimitrisLianos/LLM_Wiki_SecondBrain)

<sub>Imagen: vista social del repositorio generada por GitHub. Haz clic para abrir el repositorio.</sub>

Implementación local del patrón LLM Wiki: procesa fuentes, extrae entidades, crea Markdown enlazado y mantiene un grafo de conocimiento.

```bash
git clone https://github.com/DimitrisLianos/LLM_Wiki_SecondBrain.git
cd LLM_Wiki_SecondBrain
```

**Patrón original de Andrej Karpathy:** https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

---


[⬆️ Volver al índice](#indice-navegable)

## 11. 🔎 Webs y catálogos útiles
### AI Templates

**Web:** https://www.aitmpl.com/

Catálogo de agentes, comandos, skills, settings, hooks, MCP, mods y plugins para Claude Code. Permite revisar componentes antes de instalarlos y muestra análisis realizados con NVIDIA SkillSpector en parte del catálogo.

---

### Biblioteca de prompts — prompts.chat

**Web:** https://prompts.chat/prompts

Biblioteca pública de prompts gratuitos para ChatGPT y otros asistentes de IA. Permite explorar ejemplos por temática y reutilizarlos como punto de partida; conviene adaptar contexto, restricciones, formato de salida y criterios de validación antes de usarlos en producción.

---

### Can I run AI locally?

**Web:** https://canirun.ai/

Selector de modelos abiertos según GPU o Mac, número de aceleradores, VRAM y RAM. Clasifica qué modelos caben con margen, cuáles van ajustados y cuáles exceden el equipo, con filtros para código, imagen, vídeo y modelos pequeños. Las estimaciones dependen de la cuantización, el runtime y la configuración real.

---

### The Agent Skills Directory — Skills.sh

**Web:** https://www.skills.sh/

Directorio del ecosistema abierto Agent Skills, con buscador, tendencias, ranking de instalaciones y compatibilidad con distintos agentes. Permite instalar skills con `npx skills add`.

```bash
npx skills add propietario/repositorio
```

Antes de instalar una entrada popular, revisa el `SKILL.md`, scripts, hooks, permisos y dependencias; la popularidad no sustituye una auditoría.

---

### Modelos — LocalMaxxing

**Web:** https://localmaxxing.com/es/models

Catálogo para comparar modelos locales, variantes y fine-tunes mediante pruebas de velocidad, métricas de evaluación y configuraciones de GPU. Es útil para filtrar por hardware y contrastar rendimiento observado, pero las cifras deben revisarse junto con la cuantización, el backend y la metodología de cada prueba.

---

### Claude Code Plugins — Claude Marketplaces

**Web:** https://claudemarketplaces.com/

Directorio comunitario de skills, plugins y servidores MCP para agentes, con búsqueda, fichas, rankings por instalaciones y novedades. Sirve para descubrir componentes, no para asumir que están auditados u oficialmente respaldados: revisa siempre el repositorio, los permisos y el método de instalación.

---

### better-claude

**Web:** https://betterclaude.dev/

Colección gratuita y open source de plugins y mods para Claude Code mantenida por Midudev. Incluye utilidades de vista previa, medidores de suscripción y contexto, commits, narración y recuperación temporal, con un generador del bloque de instalación. Algunas funciones dependen del sistema operativo o de integraciones locales.

---

### Spark Plug

**Web:** https://sparkplug.sh/

Ranking de modelos abiertos que caben en uno o varios NVIDIA DGX Spark. Compara capacidad, velocidad de decodificación, receta de ejecución y resultados de benchmarks, y documenta la metodología. Es un recurso específico para hardware DGX Spark; no debe extrapolarse directamente a otras GPU.

---

### AGENTS.md

**Web:** https://agents.md/

Formato Markdown abierto para proporcionar instrucciones persistentes a agentes de programación. Funciona como un «README para agentes» con comandos de instalación, pruebas, estilo, estructura y reglas de contribución, y puede colocarse en la raíz o en subdirectorios para aplicar instrucciones por alcance.

---

[⬆️ Volver al índice](#indice-navegable)

# 🏢 Configuración empresarial recomendada de Claude Code

Guarda esta base en el `settings.json` administrado y adapta modelos, endpoints y límites a la infraestructura real.

```json
{
  "env": {
    "ANTHROPIC_MODEL": "sonnet",
    "CLAUDE_CODE_EFFORT_LEVEL": "high",
    "CLAUDE_CODE_SUBAGENT_MODEL": "haiku",

    "CLAUDE_CODE_PROMPT_CACHE_TTL": "1h",
    "CLAUDE_CODE_SUBAGENT_PROMPT_CACHE_TTL": "1h",

    "CLAUDE_CODE_MCP_ALLOWLIST_ENV": "1",
    "CLAUDE_CODE_SUBPROCESS_ENV_SCRUB": "1",
    "CLAUDE_CODE_MCP_STARTUP_WAIT_MS": "15000",
    "CLAUDE_CODE_MCP_TOOL_IDLE_TIMEOUT": "300000",
    "MCP_TOOL_TIMEOUT": "600000",
    "CLAUDE_CODE_MCP_AUTO_BACKGROUND_MS": "120000",

    "API_TIMEOUT_MS": "1200000",
    "BASH_DEFAULT_TIMEOUT_MS": "300000",
    "CLAUDE_STREAM_IDLE_TIMEOUT_MS": "600000",

    "CLAUDE_CODE_TOOL_MEMORY_LIMIT": "4G",
    "CLAUDE_CODE_WORKFLOW_MAX_CONCURRENT_AGENTS": "4",
    "CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION": "50",
    "CLAUDE_CODE_WARN_DISK_FREE_GIB": "10",
    "CLAUDE_CODE_WARN_MEMORY_FREE_GIB": "4",

    "CLAUDE_CODE_ENABLE_TELEMETRY": "1",
    "OTEL_METRICS_EXPORTER": "otlp",
    "OTEL_LOGS_EXPORTER": "otlp",
    "OTEL_EXPORTER_OTLP_PROTOCOL": "http/protobuf",
    "OTEL_EXPORTER_OTLP_ENDPOINT": "https://otel-collector.empresa.local:4318",
    "OTEL_SERVICE_NAME": "claude-code",

    "CLAUDE_CODE_PROPAGATE_TRACEPARENT": "1"
  },
  "permissions": {
    "deny": [
      "Bash(rm -rf /:*)",
      "Bash(git push --force:*)",
      "Bash(git push -f:*)"
    ]
  }
}
```

## 🎯 Variables prioritarias

1. `ANTHROPIC_MODEL`
2. `CLAUDE_CODE_EFFORT_LEVEL`
3. `CLAUDE_CODE_SUBAGENT_MODEL`
4. `CLAUDE_CODE_MCP_ALLOWLIST_ENV=1`
5. `CLAUDE_CODE_SUBPROCESS_ENV_SCRUB=1`
6. `CLAUDE_CODE_TOOL_MEMORY_LIMIT=4G`
7. `CLAUDE_CODE_WORKFLOW_MAX_CONCURRENT_AGENTS=4`
8. `CLAUDE_CODE_ENABLE_TELEMETRY=1`
9. `HTTPS_PROXY` y `NODE_EXTRA_CA_CERTS` si existe proxy corporativo
10. `CLAUDE_CODE_PROMPT_CACHE_TTL=1h`

## ✅ Recomendaciones finales

- No guardes claves API en archivos versionados.
- Usa Azure Key Vault, HashiCorp Vault, AWS Secrets Manager o el gestor corporativo equivalente.
- No actives MCP locales sin allowlist y revisión de comandos.
- Fija versiones o commits de plugins empresariales.
- Mantén la compactación automática habilitada.
- Usa modelos pequeños para exploración y tareas mecánicas.
- Reserva modelos caros y effort alto para arquitectura, seguridad, migraciones y depuración compleja.
- Envía métricas a OpenTelemetry sin registrar prompts, respuestas completas, secretos o código sensible.
- Prueba hooks, plugins y mods en un perfil aislado antes de desplegarlos al equipo.
