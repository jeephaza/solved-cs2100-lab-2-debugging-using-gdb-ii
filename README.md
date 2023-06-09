Download Link: https://assignmentchef.com/product/solved-cs2100-lab-2-debugging-using-gdb-ii
<br>
<strong>C Arrays </strong>

Array is a kind of data structure that can store a <u>fixed-size</u> sequential collection of elements of the <u>same type</u>. An array is used to store a collection of data, but it is often more useful to think of an array as a collection of variables of the same type.




Instead of declaring individual variables, such as number0, number1… and number99, you declare one array variable such as numbers and use numbers[0], numbers[1], …, numbers[99] to represent individual variables. A specific element in an array is accessed by an index which starts from 0.

All arrays consist of <u>contiguous memory locations</u>. The lowest address corresponds to the first element and the highest address to the last element.




<strong>C Functions and Arrays </strong>

In C programming, a single array element or an entire array can be passed to a function. A single value will be passed by value, whereas when passing the whole array, it is always passed as a reference to the first element of the array.




<strong> </strong>

<strong> </strong>

<strong>Objective:</strong>

You will learn how to use arrays and functions in C.




<strong>Preparation (before the lab): </strong>Please refer to lab#1.

<strong> </strong>

<strong>Procedure</strong>:

<ol>

 <li>Locate the <strong>c</strong> and <strong>lab2b.c</strong> files in the zip file that this lab document came in.</li>

</ol>




<ol start="2">

 <li>Compile <strong>c</strong> with <strong>gcc </strong>using the following command: <strong>gcc –o lab2a lab2a.c</strong></li>

</ol>




<ol start="3">

 <li>What is the output of the program? Can you change it to <strong>“2”</strong>?</li>

</ol>

<strong>Note:</strong> The output should be related to the <strong>ageArray</strong> such as an element in <strong>ageArray</strong>.




<ol start="4">

 <li>What is the purpose of the operator <strong>sizeof</strong>? What datatype will <strong>sizeof</strong> give <strong>“1”</strong> value for on all architectures?</li>

 <li>Can you get the number of elements in <strong>ageArray</strong>? To produce the following output:</li>

</ol>

<strong>2 </strong>

<strong>Size of the array is 4 </strong>

Modify the main function, write it below and show your labTA the output.

<strong>Note:</strong> The output <strong>“2”</strong> and size of array (i.e., <strong>4</strong> (<em><u>four</u></em>)) should be related to <strong>ageArray</strong> such as an element in <strong>ageArray</strong> and the number of elements in <strong>ageArray</strong>.




<table width="612">

 <tbody>

  <tr>

   <td width="612"> </td>

  </tr>

 </tbody>

</table>




<ol start="6">

 <li>Compile <strong>c</strong> with <strong>gcc </strong>using the following command: <strong>gcc –o lab2b lab2b.c</strong></li>

</ol>




<ol start="7">

 <li>Can you give 2 ways of displaying the stored value and address value of the first element of an array?</li>

 <li>Can you define the function <strong>hexToDecimal(char hex[], size_t size) </strong>in the lab2b.c <u>using pointers</u> to traverse the array? Write your function below and show your labTA the output.</li>

</ol>

<strong>Note: </strong>You are not allowed to use <strong>strtoul</strong>, <strong>strtol</strong>, or other functions from <strong>stdlib.h</strong>.

<em>Hint: Reading from the back of array is easier. Furthermore, you are already given the function </em><strong><em>hexVal(char hex) </em></strong><em>to simplify your work. </em>

<ol start="9">

 <li>Why do we pass the size of the array to the <strong>hexToDecimal</strong> function in lab2b.c? Can we calculate the size of the array inside the function?</li>

 <li>What is the format specifier to print a variable of datatype <strong>size_t</strong>?</li>

</ol>










<strong>Marking Scheme: Report – 5 marks; correct output – 5 marks; Total: 10 marks. </strong>

<strong>Program lab2a.c </strong>

<table width="620">

 <tbody>

  <tr>

   <td width="620">#include &lt;stdio.h&gt; void display(int); int main() {int ageArray[] = { 2, 15, 4 };     display(ageArray[2]);     return 0;}void display(int age) {     printf(“%d
”, age);}</td>

  </tr>

 </tbody>

</table>




<strong>Program lab2b.c </strong>

<table width="620">

 <tbody>

  <tr>

   <td width="620">#include &lt;stdio.h&gt;#include &lt;string.h&gt;#include &lt;ctype.h&gt; int hexToDecimal(char[], size_t); int hexVal(char); int main(void) {char hex[8];size_t len; printf(“Enter up to 7 hexadecimal characters: “);fgets(hex, 8, stdin);len = strlen(hex); /* End-of-Line Check */       if(hex[len-1] == ‘
’) {        len = len – 1;hex[len] = ‘ ’;} printf(“You entered: %s
”, hex);printf(“The value in decimal is: %d
”, hexToDecimal(hex, len)); return 0;}</td>

  </tr>

 </tbody>

</table>




<table width="620">

 <tbody>

  <tr>

   <td width="620"> int hexVal(char hex) {       switch(toupper(hex)) {            case ‘0’: return 0;            case ‘1’: return 1;            case ‘2’: return 2;            case ‘3’: return 3;            case ‘4’: return 4;            case ‘5’: return 5;            case ‘6’: return 6;            case ‘7’: return 7;            case ‘8’: return 8;            case ‘9’: return 9;            case ‘A’: return 10;            case ‘B’: return 11;            case ‘C’: return 12;            case ‘D’: return 13;            case ‘E’: return 14;            case ‘F’: return 15;}return 0;}int hexToDecimal(char hex[], size_t size) {// complete the function body return 0;}</td>

  </tr>

 </tbody>

</table>


