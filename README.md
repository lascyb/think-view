# think-view

- 基于 think-view 二次开发
- 本扩展不能单独使用，依赖ThinkPHP6.0+
- 具体的模板引擎配置请参考lascyb/think-template库。

## 安装

~~~
composer require lascyb/think-view
~~~
>>>---
> 相关用法基本与think/think-view 相同
>>>---

# think-view

ThinkPHP6.0 Think-Template模板引擎驱动

## 用法示例

本扩展不能单独使用，依赖ThinkPHP6.0+

首先配置config目录下的template.php配置文件，然后可以按照下面的用法使用。

~~~php

use think\facade\View;

// 模板变量赋值和渲染输出
View::assign(['name' => 'think'])
	// 输出过滤
	->filter(function($content){
		return str_replace('search', 'replace', $content);
	})
	// 读取模板文件渲染输出
	->fetch('index');


// 或者使用助手函数
view('index', ['name' => 'think']);
~~~

具体的模板引擎配置请参考think-template库。