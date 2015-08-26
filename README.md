Gulp Angular Module Renamer
====================

> Uses a regex pattern search and replace any js files with angular.modules('\*') to angular.module('ute.ui.custom') or whatever you want

![gulp-module-renamer build status](https://travis-ci.org/crivas/gulp-module-renamer.svg?branch=master)

Example

```js
var moduleRenamer = require('gulp-module-renamer');

gulp.task('module-rename', function () {

  return gulp.src('app/js/**/*.js')
    .pipe(moduleRenamer()) // will default to default module name
    .pipe(gulp.dest('dist/js'))

});
```

Example With Options
```js
var moduleRenamer = require('gulp-module-renamer');

gulp.task('module-rename', function () {

  return gulp.src('app/js/**/*.js')
    .pipe(moduleRenamer({
      newModuleName: 'custom.module.name'
      showLogs: true
    }))
    .pipe(gulp.dest('dist/js'))

});
```
