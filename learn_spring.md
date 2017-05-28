# spring
## 接口
. 用于沟通的中介物的抽象化
. 实体把自己提供给外界的一种抽象化说明，用以由内部操作分离出外部沟通方法，使其能被修改内部而不影响外界其他实体与其交互的方式
. 对应java接口即声明，声明了那些方法是对外公开提供的
## 面向接口编程
.接口设计中，分清层次以及调用关系，每层只向外提供一组功能接口，各层间仅依赖接口而非实现类
.接口实现的变动不影响各层间的调用，这一点在公共服务中尤为重要
.面向接口编程中的接口是用于隐藏具体实现和实现多态性的组件
### 接口类
	public interface OneInterface{
		String hello(String);
	}
### 实现类
	public class OneInterfaceImpl implements OneInterface{
		@Override
		public String Hello(String word){
			retrun "word from interface \'Oneinterface\":"+word;
		}
	}
### 测试类
	public static void main(String [] argss){
		OneInterface oif=new OneInterfaceImpl();
		System.out.println(oif.hello("hello"));
	}
## IOC 
.ioc：控制反转 ，控制权的转移，应用程序本事不负责依赖对象的创建和维护，而是由外部容器负责创建和维护
. di(dependy injection)是一种实现控制反转的方式
.目的：创建对象并且组装对象之间的关系
## spring 注入
.Spring 注入是指在启动Spring容器加载bean配置的时候，完成对变量的赋值行为
.常用的两种注入
	 - 设值注入
	 - 构造注入
