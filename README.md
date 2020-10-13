# NPM Packages

This repository explains how we can create and use npm packages locally for tests or prototyping purposes.

## Creating a NPM Package

1. Create a folder
2. Navigate to folder
3. run the command `npm init`

### Adding git repository

While in the folder, wun the command `git init` to start a git repository.

## Using the npm package

When the package is ready, navigate to the project where it'll be used and run the command:
`npm install path/to/npm/project`


## Simple folder structure

```cmd
.
├── dist
│   ├── colors.scss
│   └── flex.scss
├── .npmignore
├── package.json
└── README.md
```

In this example we're creating a `dist` folder that contains all our scss files.

Advantages with this is that when migrating to the official package, we won't have to change our scss files in the main project.

⚠️ Changing the package name can possible break where the reference is used.

Example of how to import this package scss file:
`@import node_modules/styles/dist/colors.scss`
