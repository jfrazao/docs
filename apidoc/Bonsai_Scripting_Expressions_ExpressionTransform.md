---
uid: Bonsai.Scripting.Expressions.ExpressionTransform
---

## summary 
'The goal of ExpressionTransform is to write one-liner expressions involving Math in a compact and efficient way.
The advantage over Python scripting is that these expressions actually get compiled down directly into C# native code rather than being interpreted, 
so there's zero overhead, making them much more performant and often simpler than the Python counterparts.

The syntax follows C#. It is possible to call all methods of the input plus all the functions of the Math class. 
The reserved keyword "it" stands for the input variable. You can also access properties and methods of the input without qualification.
For example, if you simply write "X" this will try to access the "X" property of the input.'

## Examples of scripts:
```csharp
it.Item1*it.Item2
it*2
X*X + Y*Y
Math.Abs(it)
Math.Sin(it / 100.0)
```
### convert to string
```csharp
String(it)
```
### convert to float
```csharp
Single(it)
```
### Advanced expressions to illustrate the use of the ternary operator to convert boolean to 0 or 1 integer
```csharp
it ? 1 : 0
```
### Expression to ilustrate renaming tupples
```csharp
new( it.Item1 as X, it.Item2 as Y)
```
### Advanced expressions to illustrate class construction to create a new anonymous class containing the fields Square and Sqrt
```csharp
new(it*it as Square,Math.Sqrt(it) as Sqrt)
```
### expressions to illustrate conversions
```csharp
byte(it) // 8-bit integer
char(it) // unicode character
int16(it) // 16-bit integer
int32(it) // 32-bit integer
int64(it) // 64-bit integer
single(it) // 32-bit floating point
double(it) // 64-bit floating point
decimal(it) // 128-bit floating point (see Decimal)
```