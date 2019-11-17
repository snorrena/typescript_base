Goal - create a base project structure including eslint for typescript w/prettier and airbnb rules

Steps

-   install typscript globally with npm
    npm install -g typescript

-   create a new project directory, cd into the directory and initialize a node project
    mkdir dir_name && cd dir_name && npm --init -y

-   add typscript as a local dev dependency
    npm i -D typescript or npm install --save-dev typescript

-   create the tsconfig file for transpiling typescript into javascript. This can be done in the dir when typescript has been saved globally. Adjust configs accordingly.
    tsc --init

-   add dev dependencies for eslint and related typescript plugins
    npm i eslint --save-dev

-   initialize eslint with a wizard
    ./node_modules/.bin/eslint --init

    -   if eslint is install globally I believe that the eslint --inti run in the root directory will
        include all options including the airbnb style guide

-   add dev dependencies for prettier, config and plugin
    npm i --save-dev prettier
    npm i --save-dev eslint-config-prettier eslint-plugin-prettier

-   add dev dependencies for airbnb styleguide
    npm i -D eslint-config-airbnb
    npx install-peerdeps --dev eslint-config-airbnb

-   add reference to prettier and airbnb in .esconfigrc including rules for typescript linting
-   add .prettierrc config file to root including desired rules
-   add a linting script to package.json if you would need to lint a file outside of vs code
    npm run lint path_to_file
