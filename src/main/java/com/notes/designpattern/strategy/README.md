# 策略模式

## 抽象类和接口对比
1、抽象类和接口都不能被直接实例化，如果二者要实例化，就涉及到多态，不懂多态的参见我的回答JAVA的多态用几句话能直观的解释一下吗？ - 知乎。如果抽象类要实例化，那么抽象类定义的变量必须指向一个子类对象，这个子类继承了这个抽象类并实现了这个抽象类的所有抽象方法。如果接口要实例化，那么这个接口定义的变量要指向一个子类对象，这个子类必须实现了这个接口所有的方法。

2、抽象类要被子类继承，接口要被子类实现。

3、接口里面只能对方法进行声明，抽象类既可以对方法进行声明也可以对方法进行实现。

4、抽象类里面的抽象方法必须全部被子类实现，如果子类不能全部实现，那么子类必须也是抽象类。接口里面的方法也必须全部被子类实现，如果子类不能实现那么子类必须是抽象类。

5、接口里面的方法只能声明，不能有具体的实现。这说明接口是设计的结果，抽象类是重构的结果。

6、抽象类里面可以没有抽象方法。

7、如果一个类里面有抽象方法，那么这个类一定是抽象类。

8、抽象类中的方法都要被实现，所以抽象方法不能是静态的static，也不能是私有的private。

9、接口（类）可以继承接口，甚至可以继承多个接口。但是类只能继承一个类。

10、抽象级别（从高到低）：接口>抽象类>实现类。

11、抽象类主要是用来抽象类别，接口主要是用来抽象方法功能。当你关注事物的本质的时候，请用抽象类；当你关注一种操作的时候，用接口。

12、抽象类的功能应该要远多于接口，但是定义抽象类的代价较高。因为高级语言一个类只能继承一个父类，即你在设计这个类的时候必须要抽象出所有这个类的子类所具有的共同属性和方法；但是类（接口）却可以继承多个接口，因此每个接口你只需要将特定的动作方法抽象到这个接口即可。