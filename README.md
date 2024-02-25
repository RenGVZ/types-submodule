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

Pulling in the changes from the submodule to the main repo:
Go from the main project directory into the submodule directory and run `git fetch` `git merge` to update the local code

Easier way: `git submodule update --remote {{submodule_name}}`, from your main project directory, Git will go into your submodules and fetch and update for you.

### Change submodule branch for use in main project
  git config -f .gitmodules submodule.{{submodule_name}}.branch {{branch_you_want_name}}

### Reference
https://git-scm.com/book/en/v2/Git-Tools-Submodules


