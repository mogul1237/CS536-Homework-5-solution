# CS536-Homework-5-solution

Download Here: [CS536 Homework 5 solution](https://jarviscodinghub.com/assignment/cs536-homework-5-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Homework assignments must be done individually. Collaboration on homework assignments is not allowed.
This time you will be the grader for our homework assignment 3. One of the students Ima Student tried 5
times but (sadly) none of them are correct. Recall that for homework assignment 3 we defined the language of
regular expressions as follows:
We only allow letters in regular expressions (that way we don’t have to worry about how to specifiy
characters that are the same as operators or things like newlines). As usual, we will allow ε (epsilon) in our
regular expressions. The operators for our language of regular expressions are:
| means “or” (alternation)
writing two or more things next to each other means “followed by” (catenation)
* means “zero or more” (closure or iteration)
+ means “one or more” (positive closure)
( ) are used for grouping
In a regular expression, * and + have the same, highest precedence, “followed by” has middle precedence, and
| has the lowest precedence. All of the operators are left associative.
Below are Ima’s efforts on the language of regular expressions. For each CFG, do one of the following:
a. Give one string that is a legal regular expression (given our definition above), but is not in the language
of the CFG.
b. Give one string that is not a legal regular expression (given our definition above), but is in the language
of the CFG.
c. Show that the CFG is ambiguous by drawing two different parse trees for some string in the language
of the CFG.
For cases (a) and (b), be sure to say which of the two cases you are illustrating.
Note that the terminals are LTR, EPS, OR, STAR, PLUS, LPAR, and RPAR. Note also that there is a difference
between the terminal EPS (which represents the token epsilon in our language of regular expressions) and the
symbol ε (which is used on the right-hand-side of a grammar production indicating the non-terminal on the
left-hand-side derives an empty sequence of symbols).
CFG 1:
expr → expr OR term | term
term → term item | item
item → expr STAR | expr PLUS | LTR | EPS | LPAR expr RPAR
CFG 2:
expr → LPAR expr RPAR | term
term → term OR factor | factor
factor → factor item | item
item → item STAR | item PLUS | LTR | EPS
CFG 3:
expr → expr OR term | term
term → term item | ε
item → item STAR | item PLUS | LTR | EPS | LPAR expr RPAR
CFG 4:
expr → expr OR term | term
term → term item | LPAR expr RPAR | item
item → item STAR | item PLUS | LTR | EPS
CFG 5:
expr → LTR | EPS | term
term → term OR factor | factor
factor → factor item | item
item → item STAR | item PLUS | LPAR item RPAR | expr
Handing in
Homework is to be submitted in the dropbox HW5 in Learn@uw. Please make sure that you submit the
correct homework.
