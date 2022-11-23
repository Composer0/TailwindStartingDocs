
## Installing Tailwind
npm i -D tailwindcss
npx tailwindcss init - creates tailwind.config.js


## Tailwind
tailwind.config.js allows for additional customization of the site itself.

  content: ['./*.html']  // looks for anything in the root and modifies that static sheet.

## src/input.css
### Add the following
@tailwind base;
@tailwind components;
@tailwind utilities;

you can add custom css class beneath these three.


## Once Set Up Run
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch

or...

in the json add the following script.

  "scripts": {
    "build": "tailwindcss -i ./src/input.css -o ./css/output.css",
    "watch": "tailwindcss -i ./src/input.css -o ./css/output.css --watch"
  },


// works similarly to sass.
// note instead of a css folder we could also create a distriutable folder. Learned about this folder today.

# dist/
1. The /dist stands for distributable.
2. The /dist folder contains the minimized version of the source code.
3. The code present in the /dist folder is actually the code which is used on production web applications.
4. Along with the minified code, the /dist folder also comprises of all the compiled modules that may or may not be used with other systems.
5. It is easier to add files to the /dist folder as it is an automatic process. All the files are automatically copied to the dist folder on save.
6. The /dist folder also contains all those files which are required to run/build a module for use with other platforms- either directly in the browser, or in an AMD system (eg. require.js).
7. Ideally, it is considered a good practice to clean the /dist folder before each build.