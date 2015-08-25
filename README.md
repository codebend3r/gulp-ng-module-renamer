Gulp Module Renamer
====================

Uses a regex pattern search and replace any js files with angular.modules('\*') to angular.module('ute.ui.custom') or whatever you want


    var moduleRenamer = require('gulp-module-renamer');

    gulp.task('module-rename', function () {

      return gulp.src(['app.js'])
        .pipe(moduleRenamer())
        .pipe(gulp.dest('/output'))

    });
