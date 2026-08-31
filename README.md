# Metaversus

Metaversus is a responsive animated landing page that presents a fictional
metaverse experience. It is built with the Next.js App Router, React, Tailwind
CSS, and Framer Motion.

## Tech stack

- Next.js 16
- React 19
- Framer Motion 13
- Tailwind CSS 3
- ESLint 9

## Requirements

- Node.js 24
- npm 11 or newer

## Getting started

Install the dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Available scripts

```bash
npm run dev
```

Starts the development server with Turbopack.

```bash
npm run lint
```

Runs ESLint across the project.

```bash
npm run build
```

Creates an optimized production build.

```bash
npm run start
```

Starts the production server after a successful build.

## Project structure

```text
app/          App Router pages and layouts
components/   Reusable interface components
constants/    Static content and shared data
pages/api/    API routes
public/       Images and static assets
sections/     Landing-page sections
styles/       Global styles and shared style utilities
utils/        Animation helpers
```

The main page is defined in `app/page.js`, and the global layout is defined in
`app/layout.js`.

## Code-agent guidance

`AGENTS.md` contains project instructions for compatible coding assistants.
`CLAUDE.md` forwards those instructions to Claude Code, while
`AGENTS-TEMPLATE.md` can be copied and adapted for future projects.

## Deployment

The application can be deployed to any platform that supports Next.js and
Node.js, including [Vercel](https://vercel.com/new).
