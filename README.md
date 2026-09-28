# sv

Everything you need to build a Svelte project, powered by [`sv`](https://github.com/sveltejs/cli).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```sh
# create a new project in the current directory
npx sv create

# create a new project in my-app
npx sv create my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```sh
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```sh
npm run build
```
 Couche | Technologie | Version / Description |
| :--- | :--- | :--- |
| **Front-end** | React | **v19.0** + TypeScript 5.7 |
| | Build Tool | **Vite v6.0** (remplaçant Create React App) |
| | Design / UI | **Tailwind CSS v3.4** |
| | State & Data Fetching | **TanStack Query v5**, **Axios v1.7**, **Zustand v5** |
| **Back-end** | Node.js | **v22 LTS** |
| | Framework API | **Express v5.0** + TypeScript 5.7 |
| | ORM & Base de données | **Prisma v5.22** (Database SQLite / PostgreSQL) |
| | Validation Runtime | **Zod v3.23** |
| **Test & Linting** | Vitest & ESLint | **Vitest v2.1** + **ESLint v9** |
| **DevOps & CI/CD** | Docker & GitHub Actions | **Docker Desktop**, **Docker Compose v2**, **GitHub Actions**, **SonarQube Cloud** |


You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.
