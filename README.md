# Project Setup

In main repo, add submodule with
`git submodule add {{git_url}}`

When cloning main projects for the first time which contain git submodules. you need to run the following command, if not only an empty shell submodule folder will be cloned. Command:
`git clone --recurse-submodules {{main_project_name}}`

Note for cloning pre-created submodules into existing projects:
If you already cloned the project and forgot --recurse-submodules, you can combine the `git submodule init` and `git submodule update` steps by running `git submodule update --init`. To also initialize, fetch and checkout any nested submodules, you can use the foolproof `git submodule update --init --recursive`.

Pulling in the changes from the submodule to the main repo:
Go from the main project directory into the submodule directory and run `git fetch` `git merge` to update the local code

Easier way: `git submodule update --remote {{submodule_name}}`, from your main project directory, Git will go into your submodules and fetch and update for you.

### Change submodule branch for use in main project
  git config -f .gitmodules submodule.{{submodule_name}}.branch {{branch_you_want_name}}

# To add a commit to submodule from main project
cd into submodule, you will be automatically be checkedout to the most recent commit. In order to make and push changes, checkout to erther main or develop
`gco main`
`gco develop`

### Reference
https://git-scm.com/book/en/v2/Git-Tools-Submodules


