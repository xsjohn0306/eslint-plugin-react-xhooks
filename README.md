# eslint-plugin-react-xhooks

- 拷贝react官方 [`eslint-plugin-react-hooks`](https://github.com/facebook/react/tree/master/packages/eslint-plugin-react-hooks) 插件
- 添加 `staticValueHooks` 配置
    - 配置到这里的自定义hooks, 跟useRef一样返回静态值, 不需要配置到依赖数组中

## 安装

```sh
npm install --save-dev eslint-plugin-react-xhooks
```

## 使用

- 添加插件 `markup-replace` 到 `.eslintrc` 文件的 `plugins` 中
- 添加配置 `staticValueHooks`

```json
{
  "plugins": [
    "react-xhooks"
  ],
  "rules": {
    "react-xhooks/rules-of-hooks": 2,
    "react-xhooks/exhaustive-deps": [
      2,
      {
        "staticValueHooks": "(usePersistFn|useValueRef|useInstanceRef)"
      }
    ]
  }
}
```

## License

MIT
