---
uid: Bonsai.Scripting.Expressions.ExpressionTransform
summary: 
'The goal of ExpressionTransform is to write one-liner expressions involving Math in a compact and efficient way.
The advantage over Python scripting is that these expressions actually get compiled down directly into C# native code rather than being interpreted, 
so there's zero overhead, making them much more performant and often simpler than the Python counterparts.

The syntax follows C#. It is possible to call all methods of the input plus all the functions of the Math class. 
The reserved keyword "it" stands for the input variable. You can also access properties and methods of the input without qualification.
For example, if you simply write "X" this will try to access the "X" property of the input.'
---

Examples of scripts:

it*2
X*X + Y*Y
Math.Abs(it)
Math.Sin(it / 100.0)

More advanced expressions to illustrate conversions, class construction and the use of the ternary operator:

convert boolean to 0 or 1 integer
it ? 1 : 0

convert to string
String(it)

convert to float
Single(it)

create a new anonymous class containing the fields Square and Sqrt
new(it*it as Square,Math.Sqrt(it) as Sqrt)*Please type below more information about this API:*

