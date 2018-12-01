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
│   │   └── variables.sass
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
├── .gitignore
├── package.json
└── README.md
```

### Tasks

#### Dev Tasks

These tasks are used for live reloading and debugging. They are time-saving focused. Don't use then for deploying.

- `gulp pugDev`: Compiles `pug/*.pug` into expanded `build/*.html` files. They are acessible by the name of the file, eg: `https://localhost:3000/page` for a `page.pug` file.
- `gulp sassDev`: Compiles `style.sass` and its dependencies (`assets/sass/**/*.sass`); concat result to `build/css/style.min.css` (expanded style in this step).
- `gulp jsDev`: Concat `js/*.js` into `build/js/index.min.js`.

- `gulp dev`: calls all Dev tasks

#### Build Tasks

These tasks are used for building and deploying. They are performance and good practices focused. They may be too slow for live reloading (or may cause infinite looping tasks).

- `gulp pugBuild`: Compiles `pug/index.pug` into `index.html` on root directory.
- `gulp sassBuild`: Compiles `assets/sass/style.sass` and its dependencies; autoprefix resulting css; concat result to `build/css/style.min.css`.
- `gulp jsBuild`: Concat `js/*.js` into `build/js/index.min.js`.
- `gulp imageBuild`: Optimize images (jpg, png, svg) from `assets/img` into `build/assets/img`.

- `gulp build`: Calls all Build tasks.

#### Server/Live Tasks

- `gulp watch`: Starts browsersync. Watch for chances in `.pug`, `.sass` and `.js` files. Calls dev tasks individually.
- `gulp browsersync`: Calls browsersync. Server `/` is `build/`.

#### Default tasks

- `gulp`: Calls watch. Used for dev stages.

## License

[MIT License](http://ricardogouveia3.mit-license.org/) © Ricardo Álvaro Gouveia Gomes Filho
