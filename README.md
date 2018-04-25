# dailyLearning
日常学习
## this 指向
this的指向在函数定义的时候是确定不了的，只有函数执行的时候才能确定this到底指向谁，实际上this的最终指向的是那个调用它的对象，如果找不到调用的对象  默认为window  严格模式下 this为undefined
es6箭头语法除外  es6箭头函数在定义时this指向已确定
## call，apply， bind
bind会给函数永久的绑定this
``
function returnThis () {
return this
}
var boss1 = { name: 'boss1'}
var boss1returnThis = returnThis.bind(boss1)
boss1returnThis() // boss1
var boss2 = { name: 'boss2' }
boss1returnThis.call(boss2) // still boss1
``
