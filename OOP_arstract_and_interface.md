2014/7/21
#OOP 抽象类与接口

###抽象类: 
>使用`abstract`标识抽象类和抽象方法,抽象方法没有方法体,声明时在`()`后直接加`;`,抽象类不能实例化对象,必须由子类完成所有抽象方法才能实例化对象,如果子类中还存在抽象方法,子类仍为抽象类,不能实例化对象

    abstract class Person {
        public $name;
    	public $sex;
    	public $age;
    	
    	function __construct() {
    		$this->name = $name;
    		$this->sex = $sex;
    		$this->age = $age;
    	}
    	
    	abstract function say();
    	
    	abstract function run();
    }

###接口: 
>如果抽象类中的所有方法都是抽象方法,就可以换另一种声明方式,使用接口技术,接口中不能声明变量,只能使用`const`声明常量,接口中所有成员都是`public`的,虽然 PHP 中类是单继承的,但是类可以继承多个接口

    //声明
    interface Person {
    	const CONSTANT = 'constant value';
    	function say();
    	function run();
    }
        
    //继承
    class 类名 implements 接口一, 接口二, 接口三, ... , 接口 n {
    	//实现接口中的所有抽象方法
    }
    	
    class 类名 extends 父类名 implements 接口一, 接口二, 接口三, ... , 接口 n {
    	//实现接口中的所有抽象方法
    }