# Writeup Lab 1
### By Andrew Casner and Sean
1. **Feedback**  
Needs to be completed
1. **Scala Basics: Binding and Scope**
   1. Consider the following Scala code.  
   ```Scala
   val pi = 3.14
   def circumference(r: Double): Double = {
     val pi = 3.14159
     2.0 * pi * r
   }
   def area(r: Double): Double =
     pi * r * r
   ```
   The use of `pi` at line 4 is bound at which line? The use of `pi` at line 7 is bound at which line?  
   1. Consider the following Scala code.  
   ```Scala
   val x = 3
   def f(x:Int): Int =
     x match {
       case 0 => 0
       case x => {
         val y = x + 1
         ({
           val x = y + 1
           y
         } * f(x - 1))
       }
     }
   val y = x + f(x)
   ```
   The use of `x` at line 3 is bound at which line? The use of `x` at line 6 is bound at which line? The use of `x` at line 10 is bound at which line? The use of `x` at line 14 is bound at which line?
1. **Scala Basics: Typing**  
   1. Is the Body of `g` well typed?  
   ```Scala
   def g(x: Int) = {
     val (a, b) = (1, (x, 3))
     if (x == 0) (b, 1) else (b, a + 2)
   }
   ```
1. **Run-Time Library**  
Completed
1. **Run-Time Library: Recursion**  
Completed
1. **Data Structures Review: Binary Search Trees**  
Needs to be completed
1. **JavaScripty Interpreter: Numbers**  
Needs to be completed
