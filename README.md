# eslint-config-jdsmart

## 简介

 本项目以eslint-config-airbnb-base为基础，定制出了符合团队现状的ESLint 配置。

## 添加的规则

``` javascript
 {
  'no-restricted-syntax': ['off', "BinaryExpression[operator = 'in']"],
  // don't require .vue extension when importing
  'import/extensions': ['error', 'always', {
    js: 'never',
    vue: 'never',
  }],
  'import/imports-first': 0,
  'import/no-dynamic-require': 0,
  'no-debugger': process.env.NODE_ENV === 'production' ? 2 : 0,
  'no-use-before-define': ['error', { functions: false, }],
  'no-unused-vars': 0,
  'no-console': 0,
  'no-underscore-dangle': 0,
  'arrow-parens': 0,
  'no-param-reassign': 0,
  'no-unused-expressions': 0,
  'padded-blocks': 0,
  'prefer-const': 1,
  'linebreak-style': 0,
  'max-len': 0,
  'import/no-extraneous-dependencies': 0,
 }
```