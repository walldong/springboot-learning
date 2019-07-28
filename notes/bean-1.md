# 常用注解Bean

## Controller
* Controller：用于标注控制层组件
* @Controller用于标注在一个类上，使用它标记的类就是一个SpringMVC Controller对象
* 分发处理器将会扫描使用了该注解的类的方法，并检测该方法是否使用了@RequestMapping注解
* 可以把Request请求header部分的值绑定到方法的参数上

## RestController
* @Controller和@responseBody的组合

## Component
* 泛指组件，当组件不好归类时，可以使用这个注解进行标注

## Repository 
* 用于注解DAO层，在daoimpl类上面注解
   
   * DAO：DAO层主要是做数据持久层的工作，负责与数据库进行联络的一些任务都封装在此，
   DAO层的设计首先是设计DAO的接口，然后在Spring的配置文件中定义此接口的实现类，
   然后就可在模块中调用此接口来进行数据业务的处理，而不用关心此接口的具体实现类是哪
   个类，显得结构非常清晰，DAO层的数据源配置，以及有关数据库连接的参数都在Spring的
   配置文件中进行配置。 

## Service
* 用于标注业务层组件

---

## ResponseBody
* 异步请求
* 该注解用于将Controller的方法返回的对象，通过适当的HttpMessageConverter转换为指定
格式后，写入到Response对象的body数据区
* 返回的数据不是html标签的页面，而是其他某种格式的数据时（如json，xml等）使用

## RequestMapping
* 一个用于处理请求地址映射的注解，可用于类和方法上。用于类上，表示类中的所有响应请求的
方法都是以该地址作为父路径

## AutoWired
* 它可以对内成员变量、方法及构造函数进行标注，完成自动装配的工作，通过Autowired的使用来
消除set，get方法

## PathVariable
* 用于将请求URL中的模板变量映射到功能处理方法的参数上，即取出URL模板中的变量作为参数

## RequestParam
* 主要用于在SpringMVC后台控制层获取参数，类似一种是request.getParameter("name")

## RequestHeader
* 可以把Request请求header部分的值绑定到方法的参数上

---

## ModelAttribute 
* 该Controller的所有方法在调用前，先执行此@ModelAttribute方法，可用于注解和方法参数中
可以把这个@ModelAttribute特性，应用在BaseContoller当中，所有的Controller继承
BaseController，即可实现在调用Controller时。先执行@ModelAttribute方法。

## SessionAttributes
* 即将值放在session中，写在class上面   

## Valid
* 实体数据校验，可以结合Hibernate validator一起使用

## CookieValue
* 用来获取Cookie中的值