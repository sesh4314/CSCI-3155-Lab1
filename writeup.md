# Writeup Lab 1
### By Andrew Casner and Sean Shaifubahrim
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
   #### Answer:
   `pi` at line 4 is bound at line 3<br>
   `pi` at line 7 is bound at line 1<br>
   
   This is because it is at these lines where each `pi` was implemented within their respective scopes.
   
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
   #### Answer:
   `x` at line 3 is bound at line 2<br>
   `x` at line 6 is bound at line 5<br>
   `x` at line 10 is bound at line 5<br>
   `x` at line 13 is bound at line 1<br>
   
   Similar to the reasoning for 2(a), those are where each `x` is defined for their respective scopes.

1. **Scala Basics: Typing**  
   1. Is the Body of `g` well typed?  
   ```Scala
   def g(x: Int) = {
     val (a, b) = (1, (x, 3))
     if (x == 0) (b, 1) else (b, a + 2)
   }
   ```
   #### Answer:
   Yes. Function `g` returns a tuple of the form ((Int, Int), Int).
   In line 2, we see that `a` is declared with the type `Int` and `b` is declared with the type `(Int, Int)`.
   In line 3, `g` returns either (`b`, 1) or (`b`, `a + 2`). Since `a + 2` still results in an Int, we can safely say that `g` returns a tuple with the form ((Int, Int), Int)
   
1. **Run-Time Library**  
Completed
1. **Run-Time Library: Recursion**  
Completed
1. **Data Structures Review: Binary Search Trees**  
Completed
1. **JavaScripty Interpreter: Numbers**  
Completed
