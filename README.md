# melange-basic-template

A simple project template using [Melange](https://github.com/melange-re/melange).

## Getting started

You will need [esy](https://esy.sh) package manager to obtain OCaml and Melange sources. See `esy` installation instructions [here](https://esy.sh/docs/en/getting-started.html#install-esy).

Once `esy` is available, run

```bash
esy
```

to install all dependencies and build the project.

When run, `esy` will (as specified in `esy.json`):

1. Generate a symbolically linked dir `bs-platform` in `node_modules`, which is
   necessary for JavaScript bundlers like Webpack to be able to find Melange
   stdlib JavaScript files under `node_modules/bs-platform`.
2. Build the project.
3. Use `melange`'s watch mode to rebuild files when changed.

Now you should see a `_build` folder with all generated files, you can run

```bash
node _build/default/src/Main.bs.js
```

to see the result of [`src/Main.re`](src/Main.re).

### React

This template includes React support via
[`@rescript/react`](https://github.com/rescript-lang/rescript-react). Use `npm start` to run the dev server, then open `localhost:1234` to view the app defined
in [`src/ReactApp.re`](src/ReactApp.re).
