# ngc
- Compile the angular app ahead of time (dont forget the apostrophes): "node_modules/.bin/ngc"
- This generates 25 new files
- Errors are caught ahead of time
- ngc is part of the angular cli "ng build" command. Normally, this is used, instead of vanilla ngc

# ng build
- ng build --> Builds the app without optimization into the 'dist' folder
- The output is split into different bundles. 
- Every bundle has a js file and a js.map file. The js.map file maps the js file to the source code in the various angular components
- ng build --prod --> Applies various optimizations before compiling into dist-folder (minification, uglification, dead code removal etc.)
- The contents of a dist folder are ready to be copied to a webserver and then served to the client as-is
- A hash is added to the bundle filename. This hash is changed in every build to circumevent in-browser caching and therefore forcing a reload in the client after a redeploy of the app.