# 01_CDN, Codepen

```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<div id="app">{{ message }}</div>
```

```javascript
Vue.createApp().mount('#app')
```

> Vue.js가 선택자(`#app`)를 통해서 HTML의 특정한 그 부분에서 Vue.js 문법을 사용할 수 있다. 

```js
Vue.createApp({
    _____________
}).mount('#app')
```

> `createApp` 메소드에 인수로 객체 데이터를 리터널방식으로 작성
>
> ```javascript
> Vue.createApp({
>     data: function() {
>     }
> }).mount('#app')
> ```
>
> `data` 속성에 `function` 키워드로 함수를 할당한다. 
>
> 그렇게 되면 `data` 는 속성이 아닌 메소드가 된다. 
>
> `: function()` 생략 가능하다. 
>
> ```javascript
> Vue.createApp({
>     data() {
>         return {
>             message:'Hello Vue!'
>         }
>     }
> })
> ```
>
> `data` 라는 메소드를 만들어서 객체 데이터를 하나 `return` 한다. 
>
> `message` 라는 속성을 하나 만들어서 문자 데이터(`Hello Vue`)를 할당한다. 



* 결과적으로, `Hello Vue!` 라는 문자가 손쉽게 화면에 나타날 수 있음을 알 수 있다. 

  `message` 부분의 데이터를 갱신해주면 갱신된 내용이  바로 HTML에 반영이 되어 바로 화면에 출력되고 있음을 알 수 있다. 

* 이것을 **반응성(Reactivity)** 라고 한다. 