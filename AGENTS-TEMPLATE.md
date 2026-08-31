# Plantilla reutilizable para agentes de código

> Copia este archivo en la raíz de un proyecto, renómbralo como `AGENTS.md` y
> reemplaza los campos entre corchetes. Conserva únicamente las secciones que
> aporten instrucciones reales al proyecto.

# Project instructions

## Project overview

- Nombre: `[nombre-del-proyecto]`
- Objetivo: `[descripción breve del producto]`
- Estado: `[prototipo | desarrollo | producción]`
- Gestor de paquetes: `[npm | pnpm | yarn | bun]`

## Stack

- Framework: `[framework y versión]`
- Lenguaje: `[JavaScript | TypeScript | C# | otro]`
- UI y estilos: `[Tailwind CSS | CSS Modules | otro]`
- Base de datos: `[ninguna | proveedor y versión]`
- Testing: `[Vitest | Jest | Playwright | Unity Test Framework | otro]`

## Commands

- Instalar dependencias: `[npm ci]`
- Desarrollo: `[npm run dev]`
- Lint: `[npm run lint]`
- Tests: `[npm test]`
- Compilar: `[npm run build]`

Ejecuta únicamente los comandos que existan en este proyecto. Si falta uno,
indícalo en el resumen final en lugar de inventarlo.

## Architecture

- `[carpeta/]`: `[responsabilidad]`
- `[carpeta/]`: `[responsabilidad]`
- `[carpeta/]`: `[responsabilidad]`

Respeta los límites entre capas y reutiliza módulos existentes antes de crear
otros nuevos.

## Coding rules

- Mantén el estilo y las convenciones presentes en el código cercano.
- Prioriza cambios pequeños, claros y directamente relacionados con la tarea.
- No modifiques archivos generados, dependencias instaladas ni artefactos de
  compilación.
- No agregues una dependencia si la funcionalidad ya existe en el proyecto o
  puede resolverse de forma sencilla con la plataforma.
- Preserva cambios locales que no pertenezcan a la tarea.
- No incluyas secretos, tokens ni credenciales en el repositorio.
- Documenta decisiones que no sean evidentes por el código.

## Autonomy and approvals

- Para explicar, revisar o diagnosticar, inspecciona el proyecto y comunica el
  resultado sin modificar archivos.
- Para implementar, corregir o construir, realiza los cambios locales solicitados
  y ejecuta validaciones no destructivas.
- Solicita confirmación antes de borrar datos, sobrescribir trabajo, publicar,
  desplegar, comprar o escribir en servicios externos.

## Definition of done

Antes de finalizar una implementación:

1. Ejecuta el lint configurado por el proyecto.
2. Ejecuta los tests relacionados con el cambio.
3. Ejecuta la compilación cuando corresponda.
4. Comprueba el comportamiento afectado.
5. Resume los archivos modificados, las validaciones realizadas y cualquier
   advertencia pendiente.

## Project-specific constraints

- `[restricción o decisión arquitectónica]`
- `[compatibilidad mínima requerida]`
- `[acción que el agente nunca debe realizar]`

## Next.js projects

Conserva esta sección sólo si el proyecto utiliza Next.js 16 o posterior.
Next.js puede administrar automáticamente el contenido comprendido entre los
marcadores. Agrega las reglas propias del proyecto fuera de ellos.

<!-- BEGIN:nextjs-agent-rules -->

# Next.js: read version-matched docs before coding

Antes de realizar cambios relacionados con Next.js, consulta la documentación
pertinente incluida en `node_modules/next/dist/docs/`. Esa documentación debe
tener prioridad porque coincide con la versión instalada en el proyecto.

<!-- END:nextjs-agent-rules -->

Para proyectos con App Router:

- Usa Server Components por defecto.
- Añade `"use client"` sólo cuando se necesiten hooks, eventos o APIs del
  navegador.
- Mantén rutas, layouts y metadata dentro de `app/`.
- Usa `next/image`, `next/link` y las APIs actuales del framework cuando
  correspondan.

## Optional Claude Code compatibility

Si el equipo usa Claude Code, crea también un archivo `CLAUDE.md` en la raíz
con este contenido:

```md
@AGENTS.md
```

Así los agentes compatibles comparten una única fuente de instrucciones.
