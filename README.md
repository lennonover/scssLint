# scssLint

## 命令行使用

    - 安装

    `gem install scss-lint `

    - 运行

    `scss-lint demo.scss`

## 集成到 gulp  

    使用 gulp-scss-lint

    - 安装 gulp-scss-lint

    `npm install gulp-scss-lint --save-dev`

    - 编写任务

    ```javascript
    gulp.task('scss-lint', function () {
        return gulp.src('src/**/**/*.scss')
            .pipe(cache('scsslint'))
            .pipe(scsslint({
            'config': '.scss-lint.yml'
        }));
    });
    ```

    scss-lint 有默认的配置，.scss-lint.yml 中的配置会覆盖默认配置。

## 规则
