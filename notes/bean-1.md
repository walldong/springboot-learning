# 常用注解Bean

##Controller
* Controller：用于标注控制层组件
* @Controller用于标注在一个类上，使用它标记的类就是一个SpringMVC Controller对象
* 分发处理器将会扫描使用了该注解的类的方法，并检测该方法是否使用了@RequestMapping注解
* 可以把Request请求header部分的值绑定到方法的参数上
