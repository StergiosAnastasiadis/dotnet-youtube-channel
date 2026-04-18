# Numbers, Precisions, Casting, Doubles and More

Now there is another Variable type in C# it is called **_bigint_** pretty much infinite space.

So there is `int long bigint`

In other languages like C++ is actually `longlong`

Now in C# we cannot assign a decimal number into a int variable.

There are different types of operations and methods you can do with each variable type.

Now the teachers show something like this

```
int a = (int)42.1;
int b = (int)38.2;
long c = (long)a + (long)b;
Console.WriteLine(c);
```

Now we have **_double_** and a **_float_** the difference is the same sa **_int_** and **_long_**

```
double a = 42.1;
float b = 38.2;
long c = a + b;
Console.WriteLine(c);
```

One is 32bit and the other one is 64bit

**_double_** double percision and **_float_** is Signle precision.

For Floats we get an error that we must add an F Suffix

Now we will try to add a double and a float into a double

```
double a = 42.1; // Natural Type
float b = 38.2F;
double c = checked(a + b);
Console.WriteLine(c);
```

Now with that we get a result of ***80.30000076293945***

Now there is another type which is going to do what we expect, ***decimal***

```
decimal a = 42.1M; // Explicit Type
decimal b = 38.2M;
decimal c = a + b;
Console.WriteLine(c);
```

Now the result is: ***80.3***
