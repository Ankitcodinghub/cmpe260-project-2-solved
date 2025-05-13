# cmpe260-project-2-solved
**TO GET THIS SOLUTION VISIT:** [CMPE260 Project 2 Solved](https://www.ankitcodinghub.com/product/cmpe260-project-2-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93966&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CMPE260 Project 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
In this project, you are going to implement an interpreter that will translate a statement in Yerel- Hesap language written in infix notation [1] to a statement in prefix notation (also known as Polish notation) [2]. This will help us converting arithmetic statements that we use in our daily lives to statements that can be executable by the Racket interpreter. A very simple example is shown below:

<pre>(Infix notation)
3 + 4 * 7 = 31
(3 + 4) * 7 = 49
(Prefix notation)
(+ 3 (* 4 7)) = 31
(* (+ 3 4) 7) = 49
</pre>
Notice that if you can convert an expression in infix notation into a prefix one, you can directly evaluate it in the Racket interpreter:

<pre>&gt; (eval '(+ 3 (* 4 7)))
31
&gt; (eval '(* (+ 3 4) 7))
49
</pre>
2 Language definition

We will formally define our language as a context free grammar to eliminate any ambiguity regarding the possible sentences in the language (i.e., valid arithmetic expressions). Production rules are as

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
follows:

</div>
</div>
<div class="layoutArea">
<div class="column">
Expression → Expression + Expression (1) Expression → Expression * Expression (2) Expression → (Expression) (3) Expression → (BindingList) @ (Expression) (4) Expression → number (5) Expression → variable (6) BindingList → BindingList BindingList (7) BindingList → Assignment — (8) Assignment → ‘variable := ‘variable (9) Assignment → ‘variable := number (10)

</div>
</div>
<div class="layoutArea">
<div class="column">
where number can be any valid number in Racket (e.g., 3, 2, 3.14, 3e-4) and variable is a single letter symbol (e.g., a, b, c, . . . z).

There are some special rules that set expressions in this language a little different from what we commonly use. Namely, Rule 4 introduces local scoping for variables: any Assignment in BindingList is only valid in the expression right after @.

</div>
</div>
<div class="layoutArea">
<div class="column">
2.1

• 3

•5

<ul>
<li>3</li>
<li>3</li>
<li>a</li>
</ul>
</div>
<div class="column">
Example expressions from the language

+ 4(theresultis7)

* 4 + 7 (19)

* (4 + 7) (33)

+ 7 (a valid expression, but your program should raise error if you try to evaluate)

</div>
</div>
<div class="layoutArea">
<div class="column">
<ul>
<li>(‘a := 4 –) @ (a + 7) (11)</li>
<li>a + (‘a := 4 –) @ (a + 7) (the first a is not in the scope, a valid expression, but the
program will raise error if you try to evaluate)
</li>
<li>(‘a := 7 –) @ (a * (‘a := 4 –) @ (a + 7))(nowthisisbothavalidexpression,and can be evaluated, the result is 77)</li>
<li>1 + 7 + 6 + 1 + 34 * ((‘x := 3 — ‘y := 6 –) @ (5 * (x + y + (‘z := ‘x –) @ (z)))) + 5 (2060)</li>
<li>((((((6)))))) (the result is 6)</li>
<li>(‘a := 1 — ‘b := 2 — ‘c := 3 — ‘d := 4 –) @ ((‘a := 95 –) @ ((‘d := 47 –)

@ ((‘d := 60 –) @ (a) + (‘b := 11 –) @ (69) + 38 + c + 85 + (‘b := 64 –) @ ((‘c := 89 –) @ (((‘d := 29 –) @ ((‘c := 65 –) @ (73)))) + 26) * 22 * (‘a := 65 –) @ (c + b) * (‘a := 16 –) @ (2) * b * 7 * 98 + 73 * 96 + c + 88 + (‘c := 46 —

2
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
‘d := 58 — ‘a := 13 –) @ ((‘d := 82 –) @ ((‘d := 45 –) @ ((d + d) * 52 + (‘b := 30 –) @ (81))) * (‘a := 71 –) @ (((‘d := 8 –) @ (d * 25 * c * (((‘d := 12 –) @ (b))) + 32))) * 42) + 18 * (c) + (‘c := 34 — ‘a := 98 –) @ (80) + 87 + 61 + 72)) + 36 * (((b) * 61)) + (25) + 17 * (a)) (the result is 3715593921)

You are provided with a script, generate sentence.py, that randomly samples valid sentences from this language. However, some sentences might not be evaluatable (if a symbol is not binded to any number).

3 Functions

You are going to implement six functions that will help you to parse and evaluate statements in this language.

3.1 (:= var value ) 10 points

Given a variable symbol var and a number value value, this function will return var and value

in a list. This function will be useful for parsing assignments.

Examples:

&gt; (:= ‘x 1337) ‘(x 1337)

&gt; (:= ‘y 260) ‘(y 260)

3.2 (– assignment1 assignment2 … assignmentN ) 10 points

This function will translate multiple variable assignments in this language into binding part of the let function, which would in turn help for parsing local assignments and expressions. Namely, this function constructs a new list with the first element being the keyword let and the rest being the concatenated assignments.

Examples:

&gt; (– ‘(x 3) ‘(y 14))

‘(let ((x 3) (y 14)))

&gt; (– (:= ‘x 15) (:= ‘y 92))

‘(let ((x 15) (y 92)))

&gt; (– (:= ‘x 65) (:= ‘y 35) (:= ‘z 89)) ‘(let ((x 65) (y 35) (z 89)))

3.3 (@ ParsedBinding Expr ) 10 Points

Given a parsed binding list (i.e., the output of –) and an expression, this function returns a valid let statement. You should be able to evaluate the result of this function (assuming the expression is valid).

3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Examples:

&gt; (@ ‘(let ((x 5))) ‘(x))

‘(let ((x 5)) x)

&gt; (@ ‘(let ((x 5) (y 4) (z 3))) ‘((* x y z)))

‘(let ((x 5) (y 4) (z 3)) (* x y z))

&gt; (eval (@ ‘(let ((x 5) (y 4) (z 3))) ‘((* x y z)))) 60

&gt; (@ (– (:= ‘x 5) (:= ‘y 4) (:= ‘z 3)) ‘((* x y z))) ‘(let ((x 5) (y 4) (z 3)) (* x y z))

3.4 (split at delim delim args ) 20 points

Given a list of arguments args, this function splits args by the delimiter delim and returns a list

of partitions where each partition holds arguments in between two delims. Examples:

</div>
</div>
<div class="layoutArea">
<div class="column">
&gt; (split at delim ‘a ‘(1 2 3 a 4 5 ‘((1 2 3) (4 5) (7 123))

&gt; (splitatdelim ‘+ ‘(1 2 + 3 4)) ‘((1 2) (3 4))

&gt; (splitatdelim ‘+ ‘(1 + (2 + 3) ‘((1) ((2 + 3)) (4))

&gt; (splitatdelim ‘+ ‘(1 * (2 + 3) ‘((1 * (2 + 3)) (4))

&gt; (splitatdelim ‘* ‘(1 * (2 + 3) ‘((1) ((2 + 3) + 4))

&gt; (split at delim ‘* ‘(666 123)) ‘((666 123))

</div>
<div class="column">
a 7 123))

<pre>+ 4))
+ 4))
+ 4))
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
3.5 (parse expr expr ) 30 points

This is the main function that transforms expressions in YerelHesap to expressions in Racket. Once you implement previously defined functions, this function returns a valid Racket expression which you can evaluate to get a result.

</div>
</div>
<div class="layoutArea">
<div class="column">
Examples:

&gt; (parse expr ‘(1 + 3)) ‘(+ 1 3)

&gt; (parse expr ‘(1 + x)) ‘(+ 1 x)

&gt; (parse expr ‘(3 + 4 * 7)) ‘(+ 3 (* 4 7))

&gt; (parse expr ‘(3 * 4 + 7)) ‘(+ (* 3 4) 7)

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
&gt; (parse expr ‘(3 * (4 + 7))) ‘(* 3 (+ 4 7))

&gt; (parse expr ‘(((((3 + 4)))))) ‘(+ 3 4)

<ul>
<li>&gt; &nbsp;(parse expr ‘(3)) 3</li>
<li>&gt; &nbsp;(parse expr ‘((‘x := 5 –) @ (x + 1.618)))

‘(let ((x 5)) (+ x 1.618))

&gt; (parse expr ‘((‘x := 5 –) @ ((‘x := 6 –)

‘(let ((x 5)) (let ((x 6)) (* x x)))

&gt; (parse expr ‘((‘x := 5 –) @ (x * (‘x := 6

‘(let ((x 5)) (* x (let ((x 6)) x)))

&gt; (parse expr ‘((‘x := 5 –) @ (y * (‘x := 6

‘(let ((x 5)) (* y (let ((x 6)) x)))

&gt; (parse expr ‘(1 + 7 + 6 + 1 + 34 * ((‘x :=

‘x –) @ (z)))) + 5))

‘(+ 1 7 6 1 (* 34 (let ((x 3) (y 6)) (* 5 (+ x y (let ((z x)) z))))) 5)

&gt; (parse expr ‘((‘a := 1 — ‘b := 2 — ‘c := 3 — ‘d := 4 –) @ ((‘a := 95 –) @ ((‘d := 47 –) @ ((‘d := 60 –) @ (a) + (‘b := 11 –) @ (69) + 38 + c + 85 + (‘b := 64 –) @ ((‘c := 89 –) @ (((‘d := 29 –) @ ((‘c := 65 –) @ (73)))) + 26) * 22 * (‘a := 65 –) @ (c + b) * (‘a := 16 –) @ (2) * b * 7 * 98 + 73 * 96 + c + 88 + (‘c := 46 —

‘d := 58 — ‘a := 13 –) @ ((‘d := 82 –) @ ((‘d := 45 –) @ ((d + d) * 52 + (‘b := 30 –) @ (81))) * (‘a := 71 –) @ (((‘d := 8 –) @ (d * 25 * c * (((‘d := 12 –) @ (b))) + 32))) * 42) + 18 * (c) + (‘c := 34 — ‘a := 98 –) @ (80) + 87 + 61 + 72))

+ 36 * (((b) * 61)) + (25) + 17 * (a))))

<pre>'(let ((a 1) (b 2) (c 3) (d 4))
   (+
</pre>
<pre>    (let ((a 95))
      (let ((d 47))
</pre>
<pre>        (+
         (let ((d 60)) a)
         (let ((b 11)) 69)
         38
         c
         85
         (*
</pre>
<pre>          (let ((b 64)) (+ (let ((c 89)) (let ((d 29)) (let ((c 65)) 73))) 26))
          22
          (let ((a 65)) (+ c b))
          (let ((a 16)) 2)
</pre>
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
b

7 98)

(* 73 96) c

</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
<div class="layoutArea">
<div class="column">
@ (x * x)))) –) @ (x)))) –) @ (x)))) 3 — ‘y := 6

</div>
<div class="column">
–) @ (5 * (x + y + (‘z :=

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
<pre>         88
         (let ((c 46) (d 58) (a 13))
</pre>
<pre>           (*
            (let ((d 82)) (let ((d 45)) (+ (* (+ d d) 52) (let ((b 30)) 81))))
            (let ((a 71)) (let ((d 8)) (+ (* d 25 c (let ((d 12)) b)) 32)))
            42))
</pre>
<pre>         (* 18 c)
         (let ((c 34) (a 98)) 80)
         87
         61
         72)))
</pre>
<pre>    (* 36 (* b 61))
    25
    (* 17 a)))
</pre>
(spaces, tabs, linebreaks might not be the same in your terminal)

3.6 (eval expr expr ) 20 points

This function first parses an expression expr, then evalutes it and returns the result. Once you

implement parse expr, the implementation of this function is trivial. Examples:

<ul>
<li>&gt; &nbsp;(eval expr ‘(1 + 3)) 4</li>
<li>&gt; &nbsp;(eval expr ‘(1 + x))

(You should get an error saying that x is undefined. You don’t have to implement the error output. Just make sure that the above expression raises an error.)

&gt; (evalexpr ‘(3 + 4 * 7)) 31

&gt; (evalexpr ‘(3 * 4 + 7)) 19
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
&gt; (eval expr ‘(3 * (4 + 7))) 33

<ul>
<li>&gt; &nbsp;(eval expr ‘(((((3 + 4)))))) 7</li>
<li>&gt; &nbsp;(eval expr ‘(3)) 3</li>
<li>&gt; &nbsp;(eval expr ‘((‘x 6.618

&gt; (eval expr ‘((‘x 36

&gt; (eval expr ‘((‘x 30

&gt; (eval expr ‘((‘x Error</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
:= 5 –) @ (x + 1.618)))

:= 5 –) @ ((‘x := 6 –) @ (x * x)))) := 5 –) @ (x * (‘x := 6 –) @ (x)))) := 5 –) @ (y * (‘x := 6 –) @ (x))))

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
&gt; (eval expr ‘(1 + 7 + 6 + 1 + 34 * ((‘x := 3 — ‘y := 6 –) @ (5 * (x + y + (‘z := ‘x –) @ (z)))) + 5))

2060

&gt; (eval expr ‘((‘a := 1 — ‘b := 2 — ‘c := 3 — ‘d := 4 –) @ ((‘a := 95 –) @ ((‘d := 47 –) @ ((‘d := 60 –) @ (a) + (‘b := 11 –) @ (69) + 38 + c + 85 + (‘b := 64 –) @ ((‘c := 89 –) @ (((‘d := 29 –) @ ((‘c := 65 –) @ (73)))) + 26) * 22 * (‘a := 65 –) @ (c + b) * (‘a := 16 –) @ (2) * b * 7 * 98 + 73 * 96 + c + 88 + (‘c := 46 —

‘d := 58 — ‘a := 13 –) @ ((‘d := 82 –) @ ((‘d := 45 –) @ ((d + d) * 52 + (‘b := 30 –) @ (81))) * (‘a := 71 –) @ (((‘d := 8 –) @ (d * 25 * c * (((‘d := 12 –) @ (b))) + 32))) * 42) + 18 * (c) + (‘c := 34 — ‘a := 98 –) @ (80) + 87 + 61 + 72)) + 36 * (((b) * 61)) + (25) + 17 * (a))))

3715593921

</div>
</div>
</div>
