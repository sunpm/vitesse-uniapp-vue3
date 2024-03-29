<p align='center'>
快速地<sup><em>vitesse-uniapp-vue3</em></sup> 创建 uniapp + vue3 + ts 应用
<br>
</p>

<br>

<p align='center'>
<a href="https://vitesse-uniapp-vue3.netlify.app/">🖥 在线预览</a>
</p>

## 平台兼容性
在技术考量上，优先同时支持下列的平台，为兼容多个平台而舍弃一些实用的依赖插件。如发现下列平台环境开发编译出现问题，欢迎提 [issue](https://github.com/sunpm/vitesse-uniapp-vue3/issues/new) or [pr](https://github.com/sunpm/vitesse-uniapp-vue3/pulls)

| H5 | IOS  | 安卓 | 微信小程序 | 字节小程序 | 快手小程序 | 支付宝小程序 |
|:--:| :--: | :--: | :--------: | :--------: | :--------: | :----------: |
| √  |  √   |  √   |     √      |     √      |     √      |      √       |


## 特性
- 🗂 [基于文件的路由](./src/pages)

- 📦 [组件自动化加载](./src/components)

- 🍍 [使用 Pinia 的状态管理](https://pinia.vuejs.org/)

- 📑 [布局系统](./src/layouts)

- 🔥 使用 [新的 `<script setup>` 语法](https://github.com/vuejs/rfcs/pull/227)

- 📥 [API 自动加载](https://github.com/unplugin/unplugin-auto-import) - 直接使用 Composition API 无需引入

- 🎨 [UnoCSS](https://github.com/unocss/unocss) - 高性能且极具灵活性的即时原子化 CSS 引擎

- 🦾 TypeScript, 为什么不呢

- ⚙️ 使用 [Vitest](https://github.com/vitest-dev/vitest) 进行单元测试

## 预配置

### UI 框架
- [uview-plus](https://uiadmin.net/uview-plus) uview-plus3.0是基于uView2.x修改的vue3版本
- [UnoCSS](https://github.com/unocss/unocss) 高性能且极具灵活性的即时原子化 CSS 引擎
- [unocss-preset-uni](https://github.com/uni-helper/unocss-preset-uni) 专为 uni-app 打造的 UnoCSS 预设

### 插件
- [Pinia](https://github.com/vuejs/pinia) - 直接的, 类型安全的, 使用 Composition API 的轻便灵活的 Vue 状态管理
  - [`pinia-plugin-persist-uni`](https://github.com/Allen-1998/pinia-plugin-persist-uni) - pinia 在 uniapp 中数据持久化插件
- Router
  - [`@uni-helper/vite-plugin-uni-pages`](https://github.com/uni-helper/vite-plugin-uni-pages) - 在 Vite 驱动的 uni-app 上使用基于文件的路由系统
  - [`vite-plugin-vue-layouts`](https://github.com/uni-helper/vite-plugin-uni-layouts) - 页面布局系统
- [`unplugin-vue-components`](https://github.com/antfu/unplugin-vue-components) - 自动加载组件
- [`unplugin-auto-import`](https://github.com/antfu/unplugin-auto-import) - 直接使用 Composition API 等，无需导入

### 编码风格

- 使用 Composition API 地 [`<script setup>` SFC 语法](https://github.com/vuejs/rfcs/pull/227)
- [ESLint](https://eslint.org/) 配置为 [@antfu/eslint-config](https://github.com/antfu/eslint-config) - 单引号, 无分号...
  - [@unocss/eslint-config](https://unocss.dev/integrations/eslint) - 用于UnoCSS的ESLint配置
  - [@uni-helper/eslint-config](https://github.com/uni-helper/eslint-config) - 适用于 uni-app 的 Anthony's ESLint 配置预设


## 环境建议

**Node >= 18**

[//]: # (**pnpm 8**)

## 使用该模版
```sh
npx degit sunpm/vitesse-uniapp-vue3#main my-vitesse-uniapp-vue3
cd my-vitesse-uniapp-vue3
yarn
```
[//]: # (pnpm i # 如果你没装过 pnpm, 可以先运行: npm install -g pnpm)

## 问题

报错：`Uncaught SyntaxError: The requested module '/node_modules/vue-demi/lib/index.mjs?v=701bef9f' does not provide an export named 'hasInjectionContext'`
> pinia v2.1.X 版本要求 vue 3.3 或者 vue-demi latest ，目前 uniapp 的 vue 版本是 ^3.2.45，通过 pinia 降级到 2.0.X 可以运行和使用。

## 感谢

- [vitesse](https://github.com/antfu/vitesse)
- [uni-helper](https://github.com/uni-helper)
- [uni-vitesse](https://github.com/Ares-Chang/uni-vitesse)
