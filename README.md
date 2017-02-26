# LISP

## Calculating Pi by implementing Gauss-Legendre algorithm

This assignment is made for computing the digits of pi, it will produce correct digits by doing some iterations. With the given function roundToPrecision (number precision), it will be able to round of the number to a certain precision, which is in 10000 digits on this exercise.

This solution provides few steps:

First, defining starting values for a, b, p and t based on the given formula of Gauss-Legendre. I used setf in defining mutable variables, but as what I've seen from others, defvar is also an alternative way of doing that, I just preferred to follow the example in variables.lisp :)

Then, creating functions that will calculate the next values of a, b, p and t.

And lastly, a function that works recursively in calculating pi. A nested let-binding that store values, this will end when the current pi and previous pi are equal, meaning it has already reached the most accurate pi in 10000 digits.

## FLATMAP Exercises
#### myMap
Passing a lambda function and a list as arguments of myMap, checks if list is nil - will return nil, if not it will use the cons function, having the lambda called by funcall with the first element of the list(get by car) as its first argument and  recursively call the method itself passing the rest of the list (get by cdr) as its second argument. This will return a new list of new elements which are executed by the lambda's body/operation.

#### myFlatten
Passing a list of lists as an argument of myFlatten function, checks if list is nil - will return nil, if not it will append the two list by going through each element, taking the first element and recursively call the function itself with the rest as parameter. This will return a new whole list of the combined elements in the lists.

#### myFlatMap
Passing a list of lists and a lambda as arguments of myFlatMap. This will do the same process as myFlatten, but instead of just taking the first element, it will call myMap function to execute the lambda function to the first element before appending to the new list. This will return a whole new list of combined elements after executing the lambda operation on each.


Note: (for my own reference)

* (write (coerce (calcPI a0 b0 t0 p0 0L0) 'long-float))
          coerce - type converter function
* (setf a 10)
* (let ((n 20))
  (write n)
  )
* (list 2)
* (list 2 nil)
* (cons 2 nil)
* (cons 2 (cons 4 nil))
* (append (list 1 2) (list 3 4))
* (nreverse (list 1 2 3))
* (lambda (a) (+ a 2))
* (funcall (lambda (a) (+ a 2)) 4) 
* (defun f (a) (+ a a))
* (f 10)
* T
* nil
* (if (equal (list 1 2) (list 1 2)) T nil)
