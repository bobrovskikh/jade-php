# jade-php

Для получения из файлов jade на выходе, файлы с разрешением php:

1) ставим gulp-rename
2) код

      gulp.src('../src/**/*.jade')
        .pipe(jade({
            pretty: true
        }))
        .pipe(rename(function (path) {
            path.extname = ".php"
        }))
        .pipe(gulp.dest('./out'));
        
PS пробовал логичный плагин gulp-jade-php но он не компелировал цикл, выдавал ошибку
