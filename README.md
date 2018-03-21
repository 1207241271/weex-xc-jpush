# weex-xc-jpush

<img width="110" src="http://docs.jiguang.cn/img/logo.png"/>


#### 一款Jpush weex插件，当前版本添加设置，删除Alias操作，获取通知内容接口。请配合[极光推送开发文档](http://docs.jiguang.cn/jpush/guideline/intro/)使用该插件    


#### JPush 模块
| 属性       		| 类型	     	| 示例		  | 描述              |
| ------------- 	|:---------:	| -----:	  | ----------:      |
| alias         |String       |simcom_8888|订阅的别名，根据此来进行推送服务|
| callback      | function    |           |回调函数           |
|seq 				| int			| 1231       |调用时传入的会话序列号|

+ callback 回调参数

| 属性       		| 类型	     	| 示例		  | 描述              |
| ------------- 	|:---------:	| -----:	  | ----------:      |
| code         	|int        	|601		|返回码|
|iAlias    | String    	|simcom_8888|订阅的别名|
|seq 		| int			| 1231    |调用时传入的会话序列号|

#####  setAlias(alias,callback,seq)
+ 调用此 API 来设置别名

#####  deleteAlias(callback,seq)
+ 调用此 API 来删除别名

##### getAlias(callback,seq)
+ 调用此 API 来查询当前别名

#### 使用Jpush模块

``` html 


<script>
  const Jpush = requireModule('jpush');
  module.exports = {
    data: {
      
    },
    
    methods: {
      subscribe() {
			Jpush.setAlias("simcom_865067022403441",res=>{
				console.log(res);
			},131);
		}
	}
  };
  
</script>
```
