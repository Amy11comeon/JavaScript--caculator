# JavaScript--caculator
<!DOCTYPE html>
<html>
 <head>
  <title> 事件</title>  
  <script type="text/javascript">
   function count(){
     var num1 = document.getElementById("txt1").value; 
    //获取第一个输入框的值
    var num2 = document.getElementById("txt2").value;  
	//获取第二个输入框的值
    var chr = document.getElementById("select").value; 
    num1=parseFloat(num1);
    num2=parseFloat(num2);
	//获取选择框的值
    switch(chr){
    case "+":
    var sum=num1+num2;
    break;
    case "-":
    var sum=num1-num2;
    break;
    case "*":
    var sum=num1*num2;
    break;
    case "/":
    var sum=num1/num2;
    break;
    }
  
	//获取通过下拉框来选择的值来改变加减乘除的运算法则
    document.getElementById("fruit").value=sum;
    //设置结果输入框的值 
    
   }
  </script> 
 </head> 
 <body>
   <input type='text' id='txt1' /> 
   <select id='select'>
		<option value='+'>+</option>
		<option value="-">-</option>
		<option value="*">*</option>
		<option value="/">/</option>
   </select>
   <input type='text' id='txt2' /> 
   <input type='button' value=' = ' onclick="count()" /> <!--通过 = 按钮来调用创建的函数，得到结果--> 
   <input type='text' id='fruit' />   
 </body>
</html>
