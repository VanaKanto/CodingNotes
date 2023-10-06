# JavaScript Note
该笔记仅以问答条例的形式记录本人学习过程中遇到/解决的一些疑难问题。

## 目录/快速跳转


## 暂未分类
1. **改变HTML样式颜色**

   在JavaScript中，元素的style.color属性返回的是颜色的字符串表示形式，而不是颜色的十六进制值。
   我们使用getComputedStyle(x).color来获取计算后的颜色值，并将其与rgb(255, 0, 0)进行比较，这是红色的RGB表示形式。
   请注意，即使你在CSS中使用了十六进制的颜色值，getComputedStyle也会返回RGB表示形式的颜色值。

   ```JavaScript
   function myFunction()
    {
    	x=document.getElementById("demo") // 找到元素
    	console.log(getComputedStyle(x).color);
    	if (x.style.color=="rgb(255, 0, 0)"){
    		x.style.color="#000000";          // 改变样式
    	}else{
    		x.style.color="#ff0000";          // 改变样式
    	}
    }
   ```
   
3. **isNaN()** 判定准则
   
   在JavaScript中，isNaN()函数用于确定给定的值是否是非数字（Not-a-Number）。它根据以下规则进行判断：

   - 如果传入的值是数字，返回false。
   - 如果传入的值是非数字的原始值（例如字符串、布尔值、null、undefined等），先尝试将其转换为数字，然后根据转换后的结果进行判断。
   - 如果转换后的结果是数字，返回false。
   - 如果转换后的结果是NaN，返回true。
   - 如果传入的值是一个非原始值（例如对象、数组、函数等），返回false。
   
   需要注意的是，isNaN()函数在判断时会先尝试将参数转换为数字，因此它可能产生一些意想不到的结果。例如，isNaN("123")会返回false，因为字符串"123"可以成功转换为数字123。如果你想要严格判断一个值是否为数字，可以使用typeof运算符来检查类型，或者使用正则表达式进行更精确的检查。
   ```
   isNaN(123) //false
   isNaN(-1.23) //false
   isNaN(5-2) //false
   isNaN(0) //false
   isNaN('123') //false
   isNaN('Hello') //true
   isNaN('2005/12/12') //true
   isNaN('') //false
   isNaN(true) //false
   isNaN(undefined) //true
   isNaN('NaN') //true
   isNaN(NaN) //true
   isNaN(0 / 0) //true
   isNaN(null) //false
   ```
4. x
5. xx
