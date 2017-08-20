# typescript-vscode-playground
A simple vscode starter repo for experimentation or quick coding/debugging in Typescript with a couple of nice features. Probably a nice kickoff point to get started with an easily debuggable Typescript/Node project or something like that.

Youll find an ```src/index.ts``` file ready to debug from within vscode. ```tsc``` transpiles your ```.ts``` files to ```dist/```, along with sourcemaps. You can go ahead and expand from there!

## vscode
* ```.vscode/launch.json``` is set up for debugging Typescript directly in vscode, complete with source maps, between ```src/``` and ```dist/```. Sweet.
* ```.vscode/settings.json``` excludes ```dist/``` from searches, which prevents compiled ```.js``` files from cluttering go-to-files and searches.
* I personally set shortcuts like ```meta+R``` for both ```start-debugging``` and ```restart-debugging```, and maybe ```meta+.``` to stop debugging -- all to make debugging easy to start and stop as you're coding. You can press ```meta+K meta+S``` or go to ```Preferences > Keyboard Shortcuts``` to experiment a bit and find something you're comfortable with. 
## package.json scripts
* ```tsc-watch``` is used to transpile ```src/index.ts``` -> ```dist/index.js```, and provide a codeFrame ```ts-lint``` output with each saved change. Nice. 

* ```build``` builds using the included ```tsconfig.json```. ```.js``` equivalents of ```.ts``` files are outputted to the ```/dist``` directory.

* ```clear``` removes the ```/dist``` directory recursively.

* ```lint``` runs ```tslint``` via the included ```tslint.json``` and ```tsconfig.json```, typechecks, and formats its output via codeFrame.

* ```lint-fix``` runs ```lint``` but also automatically fixes fixable issues.
