# Numbers Integers and Math

Now let's talk about integers and floating points.

`dotnet new console -n project-name -o .`

Now this below is a full and complete program

```
int a = 18;
int b = 6;
int c = a + b;
Console.WriteLine(c);
```

It has not been always like this, that is brand new since C# >= 6 or 9

That means C# the language has a version and this is .NET family of languages

The Course is at .NET 8 and C# is on version 12

Now to write code like this and run

`Console.WriteLine("Hello World!")`

This Feature is called ***Top Level Statements*** and it was introduced in .NET 6 or 9

It let's you write full programms just by typing in statements into our CS file.

So our program doesn't have to have the following

```
public static void Main {}
 ```

 And a ***Class*** program you now write ***Top Level Staments*** directly

In the old days we have a ***Main*** Function.

Now the program that we have above will work, but what if we had some big numbers.

`int a = 180000000000000000000;`

Here we get an error ***Integral constant is too large***

This is what we call squiggles

Now the Language has different ways of storing numbers, each of them dictates how big of a range they can store, storage space.

If we see the docs for ***int*** it says ***Represents a 32-bit signed integer*** so it is ***2^23***

Now if we do something like this

```
int a = 2100000000;
int b = 2100000000;
int c = a + b;
Console.WriteLine(c);
```

 we will get an output of ***-94967296***

This means we got over the rabge, overflowed

Now to solve this we can store a ***long*** which is ***64bits***

If we do it like this here, we still get ***-94967296***
```
int a = 2100000000;
int b = 2100000000;
long c = a + b;
Console.WriteLine(c);
```

Now one things to note is the difference between a ***Compiler Error***, which is like spell check

Now the above the math is happening in the integer world and it is storing the result into the long.

So we have to basically tell the compiler that despite those 2 variables are integers i want to make the calculation as a long.

So we coerce it (Type Coercion) so basically is a hard cast to a long

```
int a = 2100000000;
int b = 2100000000;
long c = (long)a + (long)b;
Console.WriteLine(c);
```

Now we can see another things here, we can use the build in function `checked()`

`long d = checked(a + b);`

This will make sure that overflow never happens, so we get a ***Runtime Exception***

So with `checked()` on Runtime the compiler can find out if the number is really big and we do not get that wrong number, we get an Error.