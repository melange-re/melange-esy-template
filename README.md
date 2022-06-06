# melange-basic-template

A simple project template using [Melange](https://github.com/melange-re/melange).

## Getting started

You will need `npm` installed, as well as the [esy](https://esy.sh) package
manager to obtain OCaml and Melange sources. See `esy` installation instructions
[here](https://esy.sh/docs/en/getting-started.html#install-esy).

To get started:

1. Run `npm install`.
2. Run `esy`.
3. For frontend development, run `npm start`.

When run, `esy` will install the OCaml-based dependencies, and, as specified in
`esy.json`:

1. Generate a symbolically linked dir `melange` in `node_modules`, which is
   necessary for JavaScript bundlers like Webpack to be able to find Melange
   stdlib JavaScript files under `node_modules/melange`.
2. Compile the ReasonML/ReScript/OCaml source files to JavaScript.
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
