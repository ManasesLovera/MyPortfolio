
This website is deployed here: https://learning-astro-with-tutorial.netlify.app/

# Astro Starter Kit: Minimal


```sh
npm create astro@latest -- --template minimal
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/minimal)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/minimal)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/minimal/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── components/
│           └── Component.astro
│   └── layouts/
│           └── BaseLayout.astro
│   └── pages/
│       └── posts/
│           └── post.md
│       └── index.astro
│   └── scripts/
│   └── styles/
├── .gitignore
├── .nojekyll
├── CNAME
└── README.md
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

## If you are deploying using Github Pages

You may have an error because github somehow guess you are using [Jekyll](https://jekyllrb.com/) and it's not able to compile, you must do the following if you are using Astro with Github Pages with custom domain:

First create a file named `.nojekyll` leave it empty and also modify the file named `astro.config.mjs` and it must look like this:
```js
import { defineConfig } from 'astro/config';

// https://astro.build/config
export default defineConfig({
    output: 'static',
    build: {
      outDir: 'docs', // Change the output directory to 'docs'
    },
    site: 'https://example.com', // Replace with your custom domain
  });
```

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## Resources

1. [Markdown cheatsheet](https://www.markdownguide.org/cheat-sheet/)
2. [YAML front matter](https://assemble.io/docs/YAML-front-matter.html)
