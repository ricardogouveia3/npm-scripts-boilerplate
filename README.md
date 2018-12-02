# NPM Scripts Boilerplate

This project uses:

- [Pug](https://pugjs.org/)
- [Sass](http://sass-lang.com/)
- [NPM](https://www.npmjs.com/)

## Getting Started

### Installation

First of all, install node.

- [NodeJS](http://nodejs.org/)

```sh

# Clone this repository
git clone git@github.com:ricardogouveia3/npm-scripts-boilerplate.git
cd npm-scripts-boilerplate

# install dependencies
npm install

```

After that, you should be good to go :)

### Folders/Files Structure

```sh
├── assets/
│   ├── sass/
│   │   ├── partials/
│   │   │   └── _*.sass
│   │   └── style.sass
│   └── img/
│       └── *.{jpg||png||svg}
├── build/
│   ├── assets/
│   │   ├── css/
│   │   │   └── style.min.css
│   │   └── img/
│   │       └── *.min.{jpg||png||svg}
│   ├── js/
│   │   └── index.min.js
│   ├── *.html
│   └── favicon.ico
├── js/
│   └── *.js
├── pug/
│   └── *.pug
├── .editorconfig
├── .eslintrc
├── .gitignore
├── package.json
├── package-lock.json
└── README.md
```

### Tasks

#### Dev Tasks

These tasks are used for live reloading and debugging. They are time-saving focused. Don't use then for deploying.

- `npm run dev`: run all dev:* tasks on parallel.

- `npm run dev:markup`: Compiles pug files into build/ with pretty sintax.
- `npm run dev:style`: run all dev-style:* on sequntial.
- `npm run dev-style:sass`: compiles sass into build/assets/css/ with pretty sintax.
- `npm run dev-style:autoprefixer`: autoprefixies resulting css file in build/assets/css.
- `npm run dev-style:rename`: renames resulting css file in build/assets/css.
- `npm run dev:js`: run dev-js:babel.
- `npm run dev-js:babel`: transpile files in js/ to index.min.js inside build/js/ (presets=es2015).

#### Build Tasks

- `build`: run all build:* tasks on parallel.

- `build:markup`: Compiles pug files into build/ with compressed sintax.
- `build:style`: run all build-style:* on sequntial.
- `build-style:sass`: compiles sass into build/assets/css/ with compressed sintax.
- `build-style:autoprefixer`: autoprefixies resulting css file in build/assets/css.
- `build-style:rename`: renames resulting css file in build/assets/css.
- `build:js`: run dev-js:babel.
- `build-js:babel`: transpile files in js/ to index.min.js inside build/js/ (presets=es2015).
- `build:images`: optimize images from assets/img to build/assets/img.

#### Server/Live Tasks

- `start`: runs watch and browsersync on parallel

- `watch`: run all watch:* tasks on parallel.
- `watch:markup`: watch for changes on pug files. exec `dev:markup`.
- `watch:style`: watch for changes on sass files. exec `dev:style`
- `watch:js`: watch for changes on js files. exec `dev:js`
- `browsersync`: start server on build/ and watch all files inside

#### Default tasks

- `start`: runs watch and browsersync on parallel

## License

[MIT License](http://ricardogouveia3.mit-license.org/) © Ricardo Álvaro Gouveia Gomes Filho
