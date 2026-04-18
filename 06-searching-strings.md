# Searching Strings

We have methods like replace
`.Replace("Hello", "Greetings");`

C# Has these function to make thigs easier, in the actual **_Core Framework_**, what we call the **_BCL_** the **_Base Class Libraries_**
That is the setup libraries build into C#
That let's you do things like string replacing

Now we have this code

```
string firstFriend = "Maria";
string secondFriend = "Scott";

string friends = $"My friends are {firstFriend} and {secondFriend}";

Console.WriteLine(friends);
```

When we put a **_._** into the end of the friends variable we get the auto suggestions.
A bunch of those have a \* in front of them

Start means that those are the most likely methods you're going to call on this object.

Now this will replace all occurrences
`Console.WriteLine(friends.Replace("Scott", "Damian"));`

Now on the code below the variable is not changing, it has to be reassinged

```
Console.WriteLine(friend);
Console.WriteLine(friends.Replace("Scott", "Damian"));
Console.WriteLine(friend);
```

We got a new string returned from Replace

The Original string value do not change

Now not all methods are like this, it depends.

Strings in C# are immutable.

That means you cannot change the contents of a string

Immutable it cannot be changed.

To mutate we have to reassing it.

Now other methods we can use are ***.Contains()*** ***.ToUpper()*** ***.Length*** ***.StartsWith('2')*** ***.EndsWith('0')***

All those methods return new String you are not changing the actual strings.

Now the compiler does not care about whitespaces and line breaks, we could add the whole program on the same line with semicolumns and it would work fine.