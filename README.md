# Hisp - A simple Lisp interpreter in Haskell

This is my first real stab at playing with Haskell. I've done some work
before to write a raycaster, but never got around to making it usable at
all--go figure! I should really get back to that at some point...

## Todo

* Build a repl

## How to use

At the moment it's pretty raw. The best thing to do is open up ghci and type
`:l Hisp`

Then you can enter expressions like:

    ghci> eval (List [List [Sym "lambda", List [Sym "x"], List [Sym "if", Sym "x", Num 1, Num 3]], Num 3]) initialEnv
    Num 1
    ghci>
   
Or, since there is now a reader, you can enter expressions like:

    ghci> eval (readVal "((lambda (x) (+ 1 x)) 41)") initialEnv
    Num 42
    ghci>
