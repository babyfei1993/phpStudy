
2014/7/20
#$_ENV 为空的原因
>`php.ini`的`variables_order`值为`GPCS`,也就是说系统在定义 PHP 预定义变量时的顺序是`GET,POST,COOKIES,SERVER`没有定义`Environment(E)`,你可以修改`php.ini`文件的`variables_order`值为你想要的顺序,如:`EGPCS`,这时,`$_ENV`的值就可以取得了

>`EGPCS`是`Environment,Get,Post,Cookies,Server`的缩写,这是 PHP 中外部变量来源的全部范围