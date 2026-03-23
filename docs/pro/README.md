# Pro版本

DataV Pro是DataV的专业版本，在原有组件库的基础上提供更多高级组件和功能。

## 安装

* npm安装

```sh
npm install @jiaminghi/data-view-pro
```

* yarn安装

```sh
yarn add @jiaminghi/data-view-pro
```

## 使用

```js
// 将自动注册所有组件为全局组件
import DataVPro from '@jiaminghi/data-view-pro'

Vue.use(DataVPro)
```

## 按需引入

```js
import { ScrollBoard } from '@jiaminghi/data-view-pro'

Vue.component(ScrollBoard.name, ScrollBoard)
```
