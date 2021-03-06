---
title: Обновление
description: Обновление Nuxt.js выполняется быстро, но требует больше усилий, чем обновление вашего package.json
position: 5
category: get-started
---

> Обновление Nuxt.js выполняется быстро, но требует больше усилий, чем обновление вашего package.json

Если вы хотите использовать статический хостинг при обновлении Nuxt v2.14 - вам понадобится добавить [target:static](/guides/features/deployment-targets#static-hosting) в ваш nuxt.config.js для корректной работы команды `generate`.

```js{}[nuxt.config.js]
export default {
  target: 'static'
}
```

## Getting Started

1. Проверьте [release notes](/guide/release-notes) для желаемой версии, чтобы узнать, есть ли какие-либо дополнительные инструкции для этого конкретного релиза.
2. Обновите версию, указанную для пакета `nuxt` в вашем файле `package.json`.

После этого шага инструкции различаются в зависимости от используемого пакетного менеджера — Yarn или NPM. _[Yarn](https://yarnpkg.com/en/docs/usage) - предпочтительный менеджер пакетов для работы с Nuxt, поскольку это инструмент разработки, для которого были написаны тесты._

## Yarn

3. удалите файл `yarn.lock` 
4. удалите папку `node_modules` 
5. выполните команду `yarn` 
6. После того как установка завершилась и вы прогнали все ваши тесты - рассмотрите возможность обновления и других зависимостей. Для этого можно использовать команду `yarn outdated`.

## NPM

3. удалите файл `package-lock.json`
4. удалите папку `node_modules`
5. выполните команду `npm install`
6. После того как установка завершилась и вы прогнали все ваши тесты - также рассмотрите возможность обновления и других зависимостей. Для этого можно использовать команду `npm outdated`.
