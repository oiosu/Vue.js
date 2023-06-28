# 03_Vue3 Webpack Template

```bash
npx degit ParkYoungWoong/webpack-template-basic vue3-webpack-template
```

> vue3 버전의 webpack 템플릿을 만들 것!

> `npx` 로 digit을 따로 설치하지 않고도 실행이 가능하다. 
>
> `ParkYoungWoong/webpack-template-basic1` : 저장소 이름 
>
> * `git clone` 과 다른 점 : 기본적인 버전 내용이 삭제가 된 상태로 복제가 된다. 따라서 새로운 프로젝트 진행 시 좋은 방법이다. 



##### ◼ vue 설치하기 

```bash
npm i vue@next
```

> `next` 를 붙여서 설치해야 다음 버전으로 설치가 된다. 
>
> 일반 의존성으로 설치해줄 것! 



##### ◼ 다른 패키지도 설치하기 

> 다른 패키지도 설치하는 이유 : vue.js 패키지인 경우에는 기본적으로 vue 문법을 해석하는 용도로 볼 수 있으며, vue 파일 자체를 관리하려면 추가적인 패키지 설치가 필요하다. 

```bash
npm i -D vue-loader@next vue-style-loader @vue/compiler-sfc
```

> 1) vue-loader@next
> 2) vue-style-loader
> 3) @vue/compiler-sfc
>
> > 개발 의존성으로 설치할것!



* `vue-style-loader` : `App.vue` 파일에서 스타일을 지정해줄 수 있는데, 내부에 있는 스타일 코드를 해석해서 동작시킬 수 있도록 만들어준다. 



##### ◼ 정상적으로 동작하는지 확인하기 

* `App.vue` 

```vue
<template>
    <h1>{{ message }}</h1>
</template>

<script>
    export default {
        data() {
            return {
                message: 'Hello Vue!!'
            }
        }
    }
</script>
```

* `main.js`

```js
import Vue from 'vue'
import App from './App.vue'

Vue.createApp(App).mount('#app')
```

* `index.html` 

```html
<div id="app"></div>
```



![image-20230628144256327](C:\Users\bestsu\AppData\Roaming\Typora\typora-user-images\image-20230628144256327.png)

```js
import { createAPP } from 'vue'
import App from './App.vue'

createApp(App).mout('#app')
```

> `Vue` 를 지워주는 대신에 `import` 다음에 위 코드 처럼 변경하기 



---

##### 🟢 다음과 같은 오류 발생 

* `npm run dev` 터미널에 명령어 작성 시 , `http://[::1]:8080/` 8080 오류 발생

* 오류 메시지 더 자세히 살펴본 결과, `error:03000086:digital envelope routines::initialization error` 라는 메시지에 대해 더 알아봄

  ![image-20230628150904254](C:\Users\bestsu\AppData\Roaming\Typora\typora-user-images\image-20230628150904254.png)

* node 17 에서 발생되는 오류 문제로 확인된다 

##### 🟢 해결방법 

```bash
npm install -g n 
```

윈도우에서는 다음과 같이 설치해준다. 

```bash
npm install -g nvm 
```

