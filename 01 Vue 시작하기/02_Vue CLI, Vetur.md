# 02_Vue CLI, Vetur

> Vue.js는 단일 페이지 애플리케이션을 빠르게 구축할 수 있는 공식 CLI를 제공한다. 
>
> #####  CLI : Command-Line Interface
>
> > CLI는 Node.js 및 관련 빌드 도구에 대한 사전 지식을 전제로 하고 있다. 
> >
> > Vue3의 경우 `npm` 에서 `@vue/cli` 로 제공되는 Vue CLI v4.5를 이용해야한다. 
> >
> > 업그레이드를 하려면 최신버전의 `@vue/cli` 를 전역으로 다시 설치해야한다. 
>
> ```bash
> yarn global add @vue/cli
> ```
>
> ```bash
> npm install -g @vue/cli
> ```

* Successfully created project `hello-vue`

* Get started with the following commands:

  ```bash
  $ cd hello-vue
  $ npm run server
  ```



---



##### ◼ App.vue

```vue
<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>
```

> 기본적인 HTML 코드 작성 부분



```VUE
<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
```

> 자바스크립트 코드 작성 부분 



```vue
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
```

> CSS 코드 작성 부분