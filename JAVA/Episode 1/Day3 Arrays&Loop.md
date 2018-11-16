# 数组
## 特点
* ==相同类型的数据的一个集合==
* ==标识符==   数组名称
* ==数组元素==  每个下标对应的值
* ==数组下标==  从0开始~数组长度减1(==防止越界==),根据数组下标获取数组中的元素
* ==元素类型==  储存元素的数据类型
## 概念
* 数组就是一个变量,用于将相同数据类型的值储存在内存中;声明数组是在内存中划分一串连续的内存空间
* 创建数组时必须指定数据类型,指定后数据类型不可变
* 数组的长度(大小)也必须指定,指定后长度不可变
* 数组中存放的数据叫做元素
* 数组中的每个元素的位置叫做下标:从0开始到数组长度减1结束,注意不要越界
## 数组声明方式
* 方式1:int[] array1 = {1,2,3,4,5,6};直接指定了数组的类型;长度;和元素的值
* 方式2:int array2 [] = {1,2,3,4,5,6};尽量不要使用这种方式
* 方式3:int[] array3 = new int[n];n表示数组的长度,指定了数组的类型和长度
* 方式4:先声明,再赋值(需要先在内存中划出内存空间,才可以使用,所以不可以用来声明方式1和方式2);float[] array4; array4 = new float[8];
## 数据类型的默认值为
* String str = "";str 有值但为空;
* 引用数据类型的默认值为null
* float的默认值为0.0
* 整型的默认值为0
* 字符型的默认值为ASCII码表中数字0所对应的值
* boolean型的默认值为flase
## 获取数组的长度
* int[] array = new int[10]; array.length;可以获取数组的长度
## 点(.)操作符的概念
* (点).后面的是属性或方法,array.length表示获取对象array的长度属性
## 第二个异常
* 数组越界异常: Java.Lang.Array.IndexOutOfBoundsException
## 数组中最后一个元素下标获取方法
* array.length - 1
## 数组使用步骤
* 1.声明
* 2.==分配空间==
* 3.赋值
* 对数组处理
## 循环结构
### while循环
* 语法: while(循环条件){ 循环体 }
 * 特点:先判断,再执行
 * 执行过程:先判断循环条件, 当循环条件为true时会执行循环体,当循环体执行完毕后,会再次执行循环条件,如果为true,会继续执行循环体代码,重复上述过程,直到某次循环的条件为false,跳出循环
 * 死循环:while(true){ 循环体}
### do-while循环
* 语法:do { 循环体 }while(条件);
* 执行过程:先执行一遍循环体,然后进行条件的判断,如果条件结果为true,则再次执行循环体,直到条件为false,跳出循环
* 特点:==至少会执行一遍循环体==
## ==for循环== 重点
* 语法: for (表达式1; 表达式2; 表达式3){   循环体 }
  * 表达式1:循环变量初始化
  * 表达式2:循环条件
  * 表达式3:循环变量的改变(自增或自减)
* 执行过程:
  * ==执行一次表达式1(只执行一次)==
  * ==判断条件(表达式2) 如果结果为true,在执行循环体,循环体执行完之后,执行表达式3,然后再执行表达式2,循环以上过程,直到表达式2为false==
* 死循环:for(;;),即表达式1,表达式2.表达式3可以省略
## ==变量的作用域==
* 基本概念: 变量生效的范围
* 使用条件: ==从变量声明开始,直到变量声明时所在的{}的末尾==
* ==在同一个作用域中==,==同一个变量不能声明两次==
## ==遍历==
* 基本概念:把数组中的每个数都取一遍