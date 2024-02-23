# Project Setup

## Step 1 Install Typescript package
`npm i typescript --save-dev`

## Step 2 Init Typesctript in project
`npx tsc --init`

## Step 3 Change tsconfig to following:
`{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "lib": ["es6"],
    "allowJs": true,
    "outDir": "build",
    "rootDir": "./src",
    "strict": true,
    "noImplicitAny": true,
    "esModuleInterop": true,
    "resolveJsonModule": true
  }
}`

## Step 4 Commit Code
gaa .
gc -m 'initial types commit'
ggp main


In main repo, add submodule with
`git submodule add {{git_url}}`

Note for cloning pre-created submodules into existing projects:
If you already cloned the project and forgot --recurse-submodules, you can combine the `git submodule init` and `git submodule update` steps by running `git submodule update --init`. To also initialize, fetch and checkout any nested submodules, you can use the foolproof `git submodule update --init --recursive`.


