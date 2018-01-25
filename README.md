# eslint-config-fhfe

[![npm version](https://badge.fury.io/js/stylelint-config-fhfe.svg)](http://badge.fury.io/js/stylelint-config-fhfe)

stylelint-config-fhfe 是烽火 UED 前端组为了帮助保持团队的代码风格统一，发现代码潜在错误而定制出了友好的 styleLint 配置。

## 使用

- 安装 stylelint

    ```
    npm install -g stylelint 
    ```

- 项目中使用

    ```
    npm install --save-dev stylelint-config-fhfe
    ```

    在你的项目根目录下创建 .stylelintrc，并将以下内容复制到文件中：

    ```javascript
    {
        extends: [
            'stylelint-config-fhfe',
        ],
        rules: {
            // 这里填入你的项目需要的个性化配置
        }
    }
    ```
    运行 

    ```
    stylelint demo.css
    ```

## 规则

    [stylelint](http://stylelint.cn/user-guide/rules/) 有百余条内置规则。它们希望为广大开发者提供更有价值的 标准 CSS 。每个规则都是独立的，默认情况下为关闭状态并没有默认值。
    
    #stylefmt 表示可以用 stylefmt 修复

- 颜色

    - color-hex-case lower	颜色值为小写字母 #stylefmt
    - color-no-invalid-hex	true	颜色值不能为无效值

- At-rule

    - at-rule-name-space-after	always	@xx 后需空格
    - at-rule-semicolon-new-new-line	alway	@xx 分号后要换行

- 函数

    - function-calc-no-unspaced-operator	true	方法中的计算符号左右需空格
    - function-comma-space-after	always	方法中逗号后需空格
    - function-linear-gradient-no-nonstandard-direction	true	linear-gradient() 内参数严格按照 css 规范
    - function-max-line-lines	0	方法中参数允许 0 行空行
    - function-parentheses-newline-inside	never-multi-line	方法中参数允许逗号后换行
    - function-url-quotes	always	地址一定要写引号
    - function-whitespace-after	always	方法之间一定要空格

- 数值

    - number-leading-zero	never	数字不以 0 开头。错误：0.5；正确：.5 #stylefmt
    - number-no-trailing-zeros	true	不能有数字末尾多余的 0。错误：1.000；正确：1 #stylefmt

- 字符串

    - string-no-newline	true	字符串之前不能有 “\n" #stylefmt 
    - string-quotes	double	字符串最外层用双引号，而不是单引号 #stylefmt

- 长度

    - length-zero-no-unit true 长度为 0 时，禁止使用单位 #stylefmt

- 单位

    - unit-case	lower	单位小写
    - unit-no-unknown	true	不允许未知的单位

- 值

    - value-keyword-case	lower	属性值小写
    - value-list-comma-newline-after	always-multi-line	属性值列不允许逗号前换行
    - value-list-comma-space-after	always	属性值列表逗号后需空格

- 简写

    - shorthand-properyu-no-redundat-values	true	可简写的属性不重复写，错误：margin: 1px 1px; #stylefmt

- 声明

    - declaration-bang-space-after	never	!important 中！后不空格
    - declatation-bang-space-before	always	!important 中！前空一格
    - declatation-colon-space-after	always	属性名冒号后空一格 #stylefmt
    - declatation-colon-space-before	never	属性名冒号前不空格 #stylefmt
    - declatation-block-no-ignored-properties	true	禁止那些由于在同一规则的另一个属性值忽略的属性值。
    - declaration-block-no-shorthand-property-overrides	true	错误：border-top-width: 1px; border: 2px solid blue;
    - declaration-block-semicolon-newline-after	always-multi-line	一个模块要么整个模块一行显示，要么分号后分行显示
    - declaration-block-semicolon-space-after	always-single-line	属性之间分号后空一格或换行
    - declaration-block-semicolon-newline-before	never-multi-line	分号前不允许换行
    - declaration-block-semicolon-space-before	never	分号前不允许空格
    - declaration-block-trailing-semicolon	always	模块内最后一个属性必须有分号

- 块

    - block-no-empty	true	不允许模块内为空
    - block-opening-brace-space-after	always-single-line	模块单行时 “{” 后空一格 #stylefmt
    - block-opening-brace-space-before	always	“{” 前空一格 #stylefmt
    - block-closing-brace-space-before	always-single-line	模块单行时 “}” 前空一格 #stylefmt

- 选择器

    - selector-attribute-brackets-space-inside	always	“[” 后空一格，“]” 前空一格
    - selector-attribute-operator-space-after	always	“[]” 内的 “=” 后空一格
    - selector-attribute-operator-space-before	always	“[]” 内的 “=” 前空一格
    - selector-combinator-space-after	always	选择器后空一格，例如：ul> li #stylefmt
    - selector-combinator-space-before	always	选择器前空一格，例如：ul >li #stylefmt
    - selector-max-compound-selectors	4	最多 4 层选择器
    - selector-no-universal	true	不允许通用选择器
    - selector-pseudo-class-case	lower	伪类选择器小写（：hover 之类）
    - selector-pseudo-class-no-unknown	true	不允许 css 规范外的伪类选择器（：hover 之类）
    - selector-pseudo-element-case	lower	伪类选择器小写（：: before 之类）
    - selector-pseudo-element-no-unknown	true	不允许 css 规范外的伪类选择器（：: before 之类）
    - selector-type-case	lower	标签选择器小写
    - selector-max-empty-lines	0	选择器共用一个模块，选择器之间允许 0 行空白
    - selector-list-comma-newline-before	never-multi-line	选择器共用一个模块，选择器之间要么一行，要么逗号后换行 #stylefmt
    - selector-list-comma-space-after	always-single-line	选择器共用一个模块，选择器一行时，逗号后空一格 #stylefmt


- 媒体规则

    - media-query-list-comma-newline-before	always-single-line	媒体查询列表中不允许逗号之前换行
    - media-query-list-comma-space-after	always-single-line	媒体查询列表中单行逗号之后空一格

- 注释

    - comment-whitespace-inside	always	注释符之间空格。正确：/* haha */

- 常用样式

    - indentation 4 缩进 4 个空格 #stylefmt
    - max-empty-lines	1	内容之间最多允许 1 行空白行
    - max-nesting-depth	4	sass 中允许嵌套的深度为 4
    - no-descending-specificity	true	选择的同一元素，不允许权重较轻的选择器出现在权重较重的之后
    - no-duplicate-selectors	true	一个样式表不允许相同的选择器出现
    - no-empty-source	true	样式表不允许为空
    - no-eol-whitespace	true	样式表末尾不允许空行
    - no-extra-semicolons	true	不允许多余的分号
    - no-invalid-double-slash-comments	false	不允许 // 注释
    - no-unknown-animations	true>	animation 的 name 不能是 keyframes 没有定义的

## 其它

- vscode [插件](https://github.com/shinnn/vscode-stylelint)
- 官方参考 [配置](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/example-config.md)
- [stylelint 中文](http://stylelint.cn/user-guide/)
		