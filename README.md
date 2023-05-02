Download Link: https://assignmentchef.com/product/solved-comp1400-lab10-working-with-global-and-local-variables
<br>
<strong>Stack Implementation: </strong>A stack, like an array, can store multiple data items of the same type. However, the operations on a stack are limited: we can either push an item onto the stack (add it to one end—the “stack top”) or pop it from the stack (remove it from the same end). Examining or modifying an item that’s not at the top of the contents is forbidden.

One way to implement a stack in C is to store its items in an array, which we’ll call contents. A separate integer variable named top marks the position of the stack top. To push an item on the stack, we simply store the item in contents at the position indicated by top, then increment top. Popping an item requires decrementing top, then using it as an index into contents to fetch the item that’s being popped<sup>*</sup>.




Based on this outline, the attached “globalContents.c” is a program that declares the contents and top variables for a stack and provides a set of functions that represent operations on the stack. All four functions need access to the top variable, and two functions need access to contents, so contents and top are declared <strong><u>globally</u></strong>.




Modify the “globalContents.c” program by moving the contents array and top into main (declare local variables), which will pass them as arguments to push, pop,

isEmpty and isFull functions as follows:




<ul>

 <li>int isEmpty(int top);</li>

 <li>int isFull(int top);</li>

 <li>int pop(int contents[], int top); – int push(int data , int contents[], int top);</li>

</ul>




Save the program in a file named as “localContents.c”, in the working directory on the PC you are using and demonstrate it to GA/TAs.

<strong> </strong>

<strong>Hint</strong>: The value of top should be updated in the main function.