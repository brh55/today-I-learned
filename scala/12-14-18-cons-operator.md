 # 12-14-2018 Cons Operator `::`
 In Scala, there is a cons operator that is short for "construct" and derived from lisp. 
 The con operator is generally used to create a list, but one thing to note is that it is _right associative_, meaning it goes right
 to left.
 
 For example you can do something like:
 ```scala
 val alphabet = 'c' :: 'b' :: 'a'
 // ("c" :: ("b" :: a) ) = List['a','b','c']
 ```
 
 Interestingly enough, when used in pattern matching, it can seperates the `head` with the "tail" (rest) of the array.
 
 ```scala
 val alphabet = 'c' :: 'b' :: 'a'
 
 def stringify(list: List[String], output: String) = list match {
  case Nil => output
  case x :: tail => x + foo(tail, x + output)
}

val abc = stingify(alphabet, "")
// 'abc'
```

As you can tell this is incredible useful for creating recursive methods such as a `reduce`.
