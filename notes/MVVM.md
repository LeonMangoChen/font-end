## MVVM（vue）三要素
#### 响应式：vue如何监听到data的每个属性变化
* 什么是响应式
> * 响应式就是修改data属性之后，vue立刻监听到
> * data属性被代理到this上

* Object.defineProperty 
>  
	var obj = {
		name: 'Leon',
		age: 25
	}
	console.log(obj.name); // 获取属性的时候，如何监听到？
	obj.age = 26;          // 赋值属性的时候，如何监听到？
>
	var obj = {};
	var _name = 'Leon';
	Object.defineProperty(obj, "name", {
		get: function () {
			console.log('get',_name); // 监听
			return _name
		},
		set: function (newVal) {
			console.log('set', newVal); // 监听
			_name = newVal;
		}
	});
	console.log(obj.name) // 可以监听到
	obj.name = 'list'; // 可以监听到

* 模拟
#### 模板引擎：vue的模板如何被解析，指令如何处理
#### 渲染：vue的模板引擎是如何被渲染成html？以及渲染过程