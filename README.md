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



