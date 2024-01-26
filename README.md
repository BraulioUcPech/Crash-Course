# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/basics)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/basics)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/basics/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

![just-the-basics]<blockquote class="imgur-embed-pub" lang="en" data-id="yInImor"><a href="https://imgur.com/yInImor">View post on imgur.com</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
// Importa el paquete mssql
const sql = require('mssql');

// Configura tus detalles de conexión
const config = {
    user: 'username',
    password: 'password',
    server: 'localhost', 
    database: 'database'
};

// Crea una función async para obtener datos
async function getData() {
    try {
        // Crea una conexión
        let pool = await sql.connect(config);
        // Realiza una consulta
        let result = await pool.request().query('SELECT * FROM table');
        // Devuelve los resultados
        return result.recordsets[0];
    } catch (err) {
        // Maneja cualquier error
        console.error(err);
    }
}

// Utiliza la función en tu componente Astro
---
const data = await getData();
---
<h1>Mis Datos</h1>
<ul>
{data.map(item => (
    <li>{item.columnName}</li>
))}
</ul>


└── 📁Crash-Course
    └── .prettierrc.mjs
    └── 📁.vscode
        └── extensions.json
        └── launch.json
    └── astro.config.mjs
    └── package.json
    └── pnpm-lock.yaml
    └── 📁public
        └── favicon.svg
        └── 📁fonts
        └── 📁img
            └── art1.jpg
            └── art2.jpg
            └── art3.jpg
            └── art4.jpg
            └── avatar.png
            └── captura-1.png
            └── dribble.png
            └── fancy-line.svg
            └── favicon.svg
            └── main-portrait.jpg
            └── paint.png
            └── paint.svg
            └── post-image.jpg
            └── scribble.svg
            └── twitter.png
        ├── styles
    └── README.md
    └── 📁src
        └── 📁components
            └── Form.tsx
            └── Gallery.astro
            └── Instro.astro
            └── Nav.tsx
            └── Testimonials.astro
            └── 📁util
                └── Scribble.astro
        └── env.d.ts
        └── 📁pages
            └── contact.astro
            └── index.astro
    └── tailwind.config.mjs
    └── tsconfig.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).
