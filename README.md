debug.js
=========

> 在手机上打印调试信息。


----------

##快速上手

	debug = require('debug');

	//debug.js为了方便调试，会默认开启捕捉浏览器的报错。如果你不需要这个功能，可以这样禁止它：
	debug.guai()


	//API
	debug.success("This is success message:)");
	debug.error("This is error message:)");
	debug.log("This is primary message:)");
	debug.log({a: 1, b: 2});
	debug.log([1,2,3]);



##DEMO

	http://binnng.github.io/debug.js/demo/index.html


##console.log

当然，如果你想继续使用console.log，可以这么封装：

	if('ontouchend' in window) {
	  console.log = debug.log.bind(debug);
	}

之后上线时，可以使用uglify压缩掉所有console的代码。完美~




