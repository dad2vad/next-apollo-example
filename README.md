# Next & Apollo Example [![Build Status](https://travis-ci.org/adamsoffer/next-apollo-example.svg?branch=master)](https://travis-ci.org/adamsoffer/next-apollo-example)

This example utilizes the [next-apollo](https://www.npmjs.com/package/next-apollo) package which is ideal if you want to tuck away some of the ceremony involved when using Apollo in your Next.js app. It also features my preferred CSS-in-JS solution, [Emotion](https://emotion.sh/).

## Demo

https://next-with-apollo.now.sh

## How to use

Install it and run

```bash
npm install
npm run dev
```

[![Deploy with ZEIT Now](https://zeit.co/button)](https://zeit.co/import/project?template=https://github.com/zeit/next.js/tree/canary/examples/with-apollo)

```bash
now
```

## The idea behind the example

Apollo - это клиент GraphQL, который позволяет легко запрашивать точные данные с сервера GraphQL. В дополнение к извлечению и изменению данных, Apollo анализирует ваши запросы и их результаты, чтобы создать кэш ваших данных на стороне клиента, который обновляется по мере выполнения дальнейших запросов и мутаций, получая больше результатов с сервера.

В этом простом примере мы без проблем интегрируем Apollo с Next, оборачивая наши страницы в компонент высшего порядка (HOC). Используя шаблон HOC, мы можем передать центральное хранилище данных результатов запроса, созданных Apollo, в нашу иерархию компонентов React, определенную на каждой странице нашего следующего приложения.

При начальной загрузке страницы, находясь на сервере и внутри getInitialProps, мы вызываем метод Apollo, getDataFromTree. Этот метод возвращает обещание; в момент разрешения обещания наш клиентский магазин Apollo полностью инициализируется.

Этот пример опирается на graph.cool для его бэкэнда GraphQL и Emotion для его решения CSS-in-JS.
