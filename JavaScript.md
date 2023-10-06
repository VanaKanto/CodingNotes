# JavaScript Note
该笔记仅以问答条例的形式记录本人学习过程中遇到/解决的一些疑难问题。

## 目录/快速跳转


## 暂未分类
1. 改变HTML样式颜色
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
   
2. xxx
3. xx
