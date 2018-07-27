# eslint-config-jdsmart

## 简介

 本项目以eslint-config-airbnb-base为基础，定制出了符合团队现状的ESLint 配置。

## 添加的规则
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

## 使用方法

安装：

  ```bash
    npm install --save-dev eslint babel-eslint eslint-config-jdsmart
  ```

在你的项目根目录下创建 `.eslintrc.js`，并将以下内容复制到文件中：

```js
module.exports = {
    extends: [
        'eslint-config-jdsmart',
    ],
    globals: {
        // 这里填入你的项目需要的全局变量
        // 这里值为 false 表示这个全局变量不允许被重新赋值，比如：
        //
        // jQuery: false,
        // $: false
    },
    rules: {
        // 这里填入你的项目需要的个性化配置，比如：
        //
        // // @fixable 一个缩进必须用两个空格替代
        // 'indent': [
        //     'error',
        //     2,
        //     {
        //         SwitchCase: 1,
        //         flatTernaryExpressions: true
        //     }
        // ]
    }
};
```

### Vue

安装：

```bash
npm install --save-dev eslint babel-eslint vue-eslint-parser@2.0.1-beta.2 babel-eslint eslint-plugin-vue@3 eslint-config-jdsmart
```

在你的项目根目录下创建 `.eslintrc.js`，并将以下内容复制到文件中：

```js
module.exports = {
    extends: [
        'eslint-config-jdsmart',
    ],
    globals: {
        // 这里填入你的项目需要的全局变量
        // 这里值为 false 表示这个全局变量不允许被重新赋值，比如：
        //
        // Vue: false
    },
    rules: {
        // 这里填入你的项目需要的个性化配置，比如：
        //
        // // @fixable 一个缩进必须用两个空格替代
        // 'indent': [
        //     'error',
        //     2,
        //     {
        //         SwitchCase: 1,
        //         flatTernaryExpressions: true
        //     }
        // ]
    }
};
```

