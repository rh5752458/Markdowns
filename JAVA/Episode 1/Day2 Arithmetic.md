## 四则运算
* 加法:0+0=0;0+1=1,1+0=1,1+1=10
* 减法:0-0=0;1-0=1,1-1=0,0-1=1
* 乘法:0×0=0，0×1=0，1×0=0，1×1=1
* 除法:0÷1=0，1÷1=1, 1÷0无意义,0÷0无意义

## 逻辑运算
为了对二进制信息进行各种处理，要使用 逻辑代数这个数学工具。逻辑代数中最基本的逻辑运算有三种：逻辑加（也称“或”运算，用符号“OR”、“∨”或“+”表示）、逻辑乘（也称“与”运算，用符号“AND”、“∧”或“·”表示）、以及取反（也称“非”运算，用符号“NOT”或“—”表示），表示如下：
* 逻辑加：0∨0=0 0∨1=1 1∨0=1 1∨1=1
* 逻辑乘：0∧0=0 0∧1=0 1∧0=0 1∧1=1
* 逻辑非：“0”取反后是“1”，“1”取反后是“0”。

## 相关转换
### 二进制转十进制
方法：“按权展开求和”
规律：个位上的数字的次数是0，十位上的数字的次数是1，......，依次递增，而十
分位的数字的次数是-1，百分位上数字的次数是-2，......，依次递减。
注意：不是任何一个十进制小数都能转换成有限位的二进制数。
### 二进制转八进制
二进制数转换成八进制数：从小数点开始，整数部分向左、小数部分向右，每3位为一组用一位八进制数的数字表示，不足3位的要用“0”补足3位，就得到一个八进制数。
【例】：10001111
010 001 111
2 1 7
所以10001111的八进制表示为（217）8.
### 二进制转十六进制
二进制数转换成十六进制数：二进制数转换成十六进制数时，只要从小数点位置开始，向左或向右每四位二进制划分一组（不足四位数可补0），然后写出每一组二进制数所对应的十六进制数码即可。
【例】：10001111
1000 1111
8 F
所以10001111的 [2]  十六进制表示为（8F）。
### 八进制转二进制
八进制转换成二进制数：八进制数通过除2取余法，得到二进制数，每个八进制对应三个二进制，不足时在最左边补充零。
【例】：127
1 2 7
001 010 111
所以127的二进制就是001010111。
### 十六进制转二进制
十六进制转二进制：十六进制数通过除2取余法，得到二进制数，每个十六进制对应四个二进制，不足时在最左边补充零。
【例】：0x8F
8 F
1000 1111
所以0x8F的二进制是10001111。 [3]


# 运算符
### 赋值运算符 =
* 把等号右边的值赋值给左边
* 表达式:符号与操作数的组合

### 算数运算符
* (+ - * / %)
* (/除法):对两个数做除法运算,结果取商
* (% 求余数):对两个数做求余运算,结果取余数
* 两个不同类型的变量进行运算,结果为精度更高的类型,也就是范围大的类型
* float 类型精度大于int
* String类型的加法运算原则是拼接字符串(就是把字符和加号的内容链接在一起)
* (++  --):(n++或者++n)代表自增(自加1),(n--或者--n)代表自减(自减1)
* i++ 表示先参与运算再生成值(自增)(i--同理)
* ++i 先生成值(自增)再参与运算

###  复合运算符
* += -+ *= /= %=
* 如 int a=3;a+=3;就表示a=a+3;其他同理
* 复合运算符会自动进行类型转换

### 交换两个变量的方法
  * 第一种:定义一个临时变量
    * 如int a=1;int b=2;int temp;
      temp=a;a=b;b=temp;
  * 第二种:加减法运算(缺点可能超过精度范围)
  * 第三种:x=x^y ;y=x^y; x=x^y;

### 比较运算符
* 比较两个值得大小关系,返回true或false(布尔类型)
* char可以当做int类型理解
* 表达式的结果也叫返回值
* 比较运算符类型由 >(大于) >=(大于等于) <(小于) <=(小于等于) !=(不等于) ==(等于)

### 三目运算符/三元运算符
* 基本语句
  * 变量=比较表达式(或结果为boolean类型的表达式)?值1(表达式):值2(表达式);(它表示如果表达式的结果为真则执行值1否则执行值2)
  * 计算三个表达式所以叫三元运算符

### 运算符优先级
* 先算小括号再算乘除后算加减

### 逻辑运算符
* 与 或 非
* 逻辑运算符是对其他的比较表达式进行运算,如判断一个变量是不是1~10之间的数;int n=5;boolean bool;bool=1=<n`&&`n<=10
* 与:`&&` 两个条件都为真结果为真
* 或:|| 两个条件中只要有一个为真结果为真
* 非:! 一目运算符 只能运算一个变量(或表达式) 直接取反
### 位运算符 对二进制做运算
* <<(左移) >>(异或) ^(异或) `&`(按位与) |(按位或)
* `&`(按位与) int x=12,y=18,z;z=x&y;(先转换为二进制,对比,都为1结果为1)如 0000 1100 与 0001 0010结果为0000 0000
* |(按位或) int x=12,y=18,z;z=x&y;(先转换为二进制,对比,有一个为1结果为1)如 0000 1100 与 0001 0010结果为0001 1110
* ^(异或) int x=12,y=18,z;z=x&y;(先转换为二进制,对比,只要每一位对比不一样结果为1)如 0000 1100 与 0001 0010结果为0001 1110
* <<(左移) 把二进制的每一位都左移,空位补0(左移几位代表原来的数乘以2的位数次方,如左移3位就是乘以8)
* (>> 右移) 在左侧空位补0即可
### 逻辑与(`&&`)与按位与(`&`)的区别
* 按位与(`&`)也可以当做逻辑运算符但与逻辑与(`&&`)有区别
* 区别 :
   * 逻辑与(`&&`) 有短路机制(如果第一个表达式的结果已经是false,那么后面的表达式不会被计算)
   * 按位与:没有短路现象
### 逻辑或(||)与按位或(|)的区别和逻辑与(`&&`)和按位与(`&`)的区别一样
### 算数异常
* 整数的除法中0不能作为除数(会报算数异常),浮点型可以(不会报异常)
## 分支结构
### java程序结构分类
  * 顺序结构
  * 分支结构(分支条件)
  * 循环结构
### if分支
  * 语法1: if(条件){ 当条件满足时执行的代码  } 条件为返回值为boolean类型的值或表达式
  * 语法2: if(条件){代码块1}else{ 代码块2}当条件满足的情况下执行代码块1否则执行代码块2
  * 语法3: if(条件1){代码块1}else if(条件2){代码块2}else if(条件3){代码块3}...else if(条件n){ 代码块n}else{   }  可以有很多else if(){  }结构
  * 语法4:if嵌套 多重if条件语句
### 如何判断两个字符窜是否相等
#### String sex = "男"; sex.equals("男") 需要调用equals方法,不能使用
### switch 分支
#### 语法
    switch(表达式){  表达式的结果必须可以自动转换为int型
        case 值1: 当表达式的结果为值1时执行代码块1;
        代码块1;
        break;  当执行完代码块1时 跳出switch结构,如果没有break,会顺序往下执行下一个case,直到遇到break为止或switch结构结束为止(即如果没有break,也会执行代码块2,如果case 2也没有break会继续往下执行,直到遇到break为止或switch结构结束为止);
        case 值2:
        代码块2;
        break;
        case 值n:
        代码块n;
        break;
        default:       如果以上条件都不满足就会执行dufault中的代码块
        代码块;
        break;



    }
### switch 和if分支结构的区别
* 所有的switch可以用if代替,反过来并不是所有的if都可以用switch代替
* jdk1.5之后switch(条件)条件支持String(字符串类型)和枚举类型