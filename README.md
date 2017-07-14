## jshint-visual-studio-reporter

JSHint Visual Studio 2015 reporter

This is a fork of [jshint-visual-studio-2015](https://github.com/jaybz/jshint-visual-studio-2015), which is a fork of [jshint-visual-studio](https://github.com/patricklafrance/jshint-visual-studio).

[jshint-visual-studio-2015](https://github.com/jaybz/jshint-visual-studio-2015) forces every message to be classified as an error in the VS Error List, even if it is a warning. This fork includes the possibility of warnings and information messages, as well an option to treat all warnings as errors. This can be passed to the reporter by passing an object with the `TreatWarningsAsErrors: true` setting.

### Usage
Using the JSHint CLI
```
jshint test.js --reporter=.\PATH-TO-DIR\jshint-visual-studio\visual-studio.js
```
Using the [gulp-jshint](https://github.com/spalger/gulp-jshint) package
```
const jshint = require('gulp-jshint');
const gulp   = require('gulp');

gulp.task('lint', function() {
  return gulp.src('./lib/*.js')
    .pipe(jshint())
    .pipe(jshint.reporter('jshint-visual-studio-reporter', { TreatWarningsAsErrors: true }));
});
```

Please refer to [jshint-visual-studio](https://github.com/patricklafrance/jshint-visual-studio) for further documentation.

### License

Thanks to Patrick Lafrance for [jshint-visual-studio](https://github.com/patricklafrance/jshint-visual-studio).

MIT © Colin Ashburn
