## ES6模块化如何使用，开发环境如何打包
* 模块化的基本语法
> export语法
>>
	/* util1.js */
	export default {
		a:100
	}
>>
	/* util2.js */
	export funciton fun1() {
		alert('fn1')
	}
	export funciton fun2() {
		alert('fn2')
	}

> inport语法
>>
	/* index.js */
	import util1 form './util1.js'
	import { fn1, fn2} form './util2.js'
>>	
	console.log(util1);
	fn1();
	fn2();

* 开发环境配置
* 关于JS众多模块化标准