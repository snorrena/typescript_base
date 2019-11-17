the following instruction detail how to manage compilation and output direction of typescript files

Installation

    npm install -g typescript - installs the latest typescript version globally


compile a .ts file to a .js file in the same dir

    tsc test.ts


to compile multiple .ts files

    tsc file1.ts file2.ts

    or

    tsc *.ts


to compile and redirect the js file(s) to another folder

    tsc myfile.ts --outDir ~/path_to_output_dir
    or

    tsc *.ts --outDir ~/path_to_output_dir


to compile multiple .ts files into a single .js and move to another folder (add --watch to recompile on saved changes)

    tsc *.ts --out ./out/app.js --watch

to compile individual .ts files in a folder and output all to another folder (add --watch to recompile on saved changes)

    tsc *.ts  --outDir ./out --watch
