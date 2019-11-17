Goal set up a env to compile and node express app from typescript to js and monitor and serve over http
including typescript-eslint and prettier

-  install local depedencies to be used in our simple web server program

express is installed as app local while the others are only require for development

i = install -D = development

    npm i express

    npm i -D typescript ts-node nodemon @types/node @types/express

    // note typescript is also installed as a development dependency inside the project

run tsc to compile all files into javascript files in the dist dir as per instructions defined in
the tsconfig.json file

three scripts listed in the package.json file manage build and deploy of the app (start, dev, build)


npm run dev

    runs the dev script in the package.json folder which uses ts.nodemon to run the express http server and the typscript program srv/app.ts and monitor for relaunch on detection of coding changes.

the server output can be seen on
    localhost:5000

npm run build

    to run the build script to compile the app.ts file into javascript as per our tsconfig and place in the dist folder
    change the target build parm in the tsconfig if it is necessary to compile to a lower version of javascript (ie ec5)

npm run start
    to run the compiled app from the dist folder

control c in the console screen to stop the running application
