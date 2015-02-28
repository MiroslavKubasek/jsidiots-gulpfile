# jsidiots-gulpfile
**A gulpfile.js for JS idiots (like me)**

This is a gulpfile that simply works, is easy to understand and aimed at webdevelopers starting a new website project - without the fancy stuff (yes, I am talking about you, Browserifiers).

**What it does for you**
* uses sass (supporting the scss-syntax) and minifies your css for production
* autoprefixes your css-file depending on your choice of browsers you want to support
* autorefreshes browsers and brower-synchronisation
* concatenates, minifies and lints your js-files
* creates all the files needed for production in the build directory
* minifies images (jpg, png, jpg, svg)
* tests the pagespeed of your site
* includes various icon references for touch devices and a favicon.ico as a reminder
* If there is a syntax error in your sass code, it won't crash (but an error message will
  be displayed instead (using gulp-plumber).

**directory structure**

`/src`: put all your code and images here. Be careful not to put code into 'src/js/main.js' (s. below).
`/build`: will contain all the files ready for production. To automatically generate them, use `gulp production`.

You can easily change the names of your source and build folder on the first two lines of gulpfile.js according to your own preferences.


**gulp commands**
* `gulp`: starts the server (using browsersync so that you can easily test your sites on all devices available). Refreshes the browsers automatically when you edit and save your scss, js or index.html files. Use this command while working on your project.
* `gulp production`: generates and copies all the files you need for deployment into the build folder
* `gulp clear`: deletes all files in your build folder
* `gulp pagespeed`: tests the speed of your site with google page speed (make sure to edit the name of your live site in your gulpfile)
* `gulp lint` checks your JS-code (and is invoked every time you change any of your JS-files)

**JS files**

All JS-files in your 'src/js' folder get concatenated into 'src/js/main.js'. JS-files in 'src/js/lib' will appear first.

**Wanna contribute?**

I would highly appreciate your contributions. Especially, if you could please help me to make the gulpfile more readable and more quality code (read: real JS). New tasks and features, however, will most likely not be added in order to keep things simple (and in line with the repository's intention/name).

**Credits**

The idiot's gulpfile is based on Google's [web-starter-kit](https://github.com/google/web-starter-kit) and [greypants' gulp starter](https://github.com/greypants/gulp-starter). Thank you for your great work and inspiration!


