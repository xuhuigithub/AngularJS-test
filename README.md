## 第一天:

### MVC
>  MVC 软件设计核心，Model(数据模型，例如Child_Parent_Scope.html中的person对象)  
>  View(视图，将后端数据模型通过模板变量的方式调用并展示)  
>  Controller(建立在Model 和 View中的一座桥梁，在AngularJS中起到了至关重要的作用，因为涉及到了$scope(作用域)。也可以在Controller中写一些业务逻辑，例如Controller_demo.html中的add 和 subtract 函数)   
### Scope：
>  最好不要在根作用域($rootScope)做修改  
>  每个作用域有自己的脏值检测  
>  作用域有点类似于namespace 不过子的作用域可以继承父作用域的东西(书中并没有提及继承，但是说到了子作用域如果查找没有的对象可以顺着父作用域一直向上寻找，直到抵达$rootScope)  
>  子作用域可以修改父作用域中的对象(例如Child_Parent_Scope.html中的person对象)  

### Controller
>  在创建控制器或者指令时，AngularJS会调用$injector(注入器)创建一个新的作用域,并在这个新建的控制器或者指令运行时将作用域当做参数传递进去。(也就是说每一个控制器都会用于自己独立的一个$scope)
>  控制器应尽可能保持短小精悍(在控制器中进行DOM操作是一个不好的实践)  