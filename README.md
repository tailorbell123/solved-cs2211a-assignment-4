Download Link: https://assignmentchef.com/product/solved-cs2211a-assignment-4
<br>
<h1>Program 1 (35 marks)</h1>

The area of a circle of radius <em>r</em> is given by

<em>                                           Area of a circle =</em> <em>π × r<sup>2</sup></em>.

Imagine that you divided this circle exactly into 4 quadrants. The area of one quadrant is then <em>0.25 × π × r<sup>2</sup>. </em>

Let us set the radius of this circle to be <em>r = 1</em>. The equation hence becomes

<em>Area of one quadrant of a circle of radius 1</em> =<em> 0.25 × π</em>.

We can simply say:

<em>π = 4 × the area of one quadrant of a circle of radius 1. </em>

To calculate the area of the shaded quadrant of the circle, use a random number generator <em><sup>x </sup></em>and guess effectively the correct value of the constant <em>π</em>. The technique you should use is to:

<ul>

 <li>Generate a random number between 0.00 and 1.00 and assign it to <em>x</em>.</li>

 <li>Generate a random number between 0.00 and 1.00 and assign it to <em>y</em>.</li>

 <li>If <em>(x<sup>2</sup>+y<sup>2</sup> &lt;= 1), </em>it means that this <em>(x,y)</em> coordinate lies <em>inside</em> the shaded quadrant.</li>

 <li>Repeat these steps <em>N</em> times, where <em>N</em> is <em><u>sufficiently large number</u></em> and then calculate the ratio of the points located inside the circle to an the total number of generated points, i.e., <em>N</em>. This ratio should approximate the area of one quadrant of this circle.</li>

 <li>Multiply the calculated ratio by 4 to find an approximation of the mathematical constant π.</li>

</ul>




Using the above procedure, draw a <em><u>flowchart</u></em> and write a <em><u>C program</u></em> to approximate the mathematical constant π.

Your program must read and validate the value of <em>N (a positive integer)</em> from the user at the beginning of execution.

Add as many inline comments as you can to make your program well documented and easy to be understood by anyone who reads it.  o Test your program using

<em>          N = 10</em>, <em>N = 100, N = 1`000, N = 100`000, N = 1`000`000, N = 10`000`000, and N = 100`000`000.</em> o Loop inside your program to <em>recalculate</em> the value of <em>π</em> <em><u>10 times</u></em> using each of the above values of <em>N</em>. Calculate the <em><u>mean</u></em> (i.e., the average value) and <em><u>standard deviation</u></em> for <em><u>results generated from the same value</u> <u>of N</u></em>. Report all results (i.e., 70 values, 7 means and 7 standard deviations).

o Discuss your results.

∑




<h1>Program 2 (30 marks)</h1>

<em>Draw a <u>flowchart</u></em> and write a <em><u>C program</u></em> that prints an <em>n×n magic square</em> (a square arrangement of the numbers <em>1, 2, …, n<sup>2</sup></em> in which the sum of the elements in any row, column, or diagonal is the same). This program should generate a magic square of a specified size <em>n</em>, where the user will specify this size at run time. The size must be an <em>odd positive</em> integer number between 1 and 13 (to be validated by your program). You should store the magic square in a two-dimensional array.

Start by placing the number <em>1</em> in the middle of row 0. Place each of the remaining numbers <em>2, 3, …, n<sup>2</sup></em> by moving <em>up one row</em> and <em>left one column</em>. Any attempt to go outside the bounds of the array should wrap around to the opposite side of the array. For example, if <em>row = 0</em>, instead of storing the next number in <em>row </em><em>-1</em>, we would store it in <em>row </em><em>n-1</em> (the last row). If <em>column = </em><em>n-1</em>, instead of storing the next number in <em>column </em><em>n</em>, we would store it in <em>column </em><em>0</em>. In addition, if a particular array element is already occupied (filled), put the number directly below the previously stored number. Here it is a sample output:

<table width="697">

 <tbody>

  <tr>

   <td width="331">


    <table width="326">

     <tbody>

      <tr>

       <td width="326">Enter size of magic square: 6Invalid size, try again…Enter size of magic square: 38    1    63       5    74       9    2</td>

      </tr>

     </tbody>

    </table></td>

   <td width="366">


    <table width="360">

     <tbody>

      <tr>

       <td width="360">Enter size of magic square: 517       24       1        8       1523        5       7       14       164        6      13       20       2210             12      19       21        311             18      25        2        9</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

In your program, you are <strong><em><u>NOT allowed</u></em></strong> to use the array notation, other than declaring the array. I.e., you can have int magic_square[12][12];

Yet, you are not allowed to use magic_square[i][j] to access the array elements in your program. Instead, you have to use the pointers notation to access the array elements.

Add as many inline comments in your program as you can to make it well documented and easy to be understood by anyone who reads it.

You should include enough <em>actual</em> test cases in your submission to demonstrate the functionality of your program, e.g., run your program with <em>n = 1, 3, 4, 5, 11, and </em><em>13</em>.

<strong> </strong>

<h1>Program 3 (35 marks)</h1>

<em>Draw a <u>flowchart</u></em><strong> and </strong><em><u>write a C function</u></em> that determines the smallest number of $20, $10, $5, $2, and $1 bills/coins necessary to pay a dollar amount. The <em><u>function prototype</u></em> must be as follow:

void pay_amount(int dollars, int *twenties, int *tens, int *fives, int

*toonies, int *lonnie);

where the dollar amount is represented by the dollars parameter. The twenties parameter points to a variable in which the function will store the number of $20 bills required. The tens, fives, toonies and lonnie parameters are similar.

You should add as many <em><u>inline comments</u></em> as you can to make your code well documented and easy to be understood by anyone who reads it.

To test your function, <em><u>write a program</u></em> that asks the user to enter an integer value (a dollar amount), calls pay_amount to get the smallest number of bills/coins necessary to pay the amount, and then display the values returned by the function.

You should include enough <em>actual</em> test cases in your submission (i.e., a cut and paste from actual run to your program) to demonstrate the functionality of your program, to test various cases <strong><em><u>(at least 8 different cases)</u></em></strong>.