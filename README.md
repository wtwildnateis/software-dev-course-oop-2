# Java OOP - Method Overloading and Static Methods

## Introduction

In this exercise, you will work on a `LemonadeStand` application that simulates 
a lemonade stand.   The menu system and main application is already implemented
in the `Main` class, but the `LemonadeStand` class and the `Lemonade` class both
need some work to support some additional functionality.

Let's get started!

## Familiarize Yourself with the Code

Before you begin, take a moment to familiarize yourself with the code that is
already implemented.  Open the `Main` class in the `src/main/java/org/example`
directory and take a look at the `Main` class.  You will see that this class
implements a simple menu system that allows the user to interact with the
`LemonadeStand` application.

Look through the menu code to see what options are available to the user.

You will also see that the `LemonadeStand` class is already implemented, but
has a commented section that indicates that we will need to add an overloaded
implementation of the `sellLemonade` method.

Finally, you will see that the `Lemonade` class is already implemented, but
has a commented section that indicates that we will need to add a static
method allowing us to create a new `Lemonade` object by mixing two other
`Lemonade` objects.

## Adding `sellLemonade` Method Overload

The `LemonadeStand` class has a method called `sellLemonade` that allows the
user to sell lemonade.  This method is already implemented for selling a normal
lemonade, but we need to add an overloaded version of this method that allows
the user to sell a special lemonade where the user has selected the amount of
lemons, sugar, and ice to use.

Remmember that method overloading allows us to define a new method with the
same name as an existing method, but with different parameters.  In this case,
we want to add a new method called `sellLemonade` that takes three parameters
(in this order!):

| Parameter | Type   | Description              |
|-----------|--------|--------------------------|
| lemons    | int    | The number of lemons to use in the lemonade |
| sugar     | int    | The amount of sugar to use in the lemonade |
| ice       | int    | The amount of ice to use in the lemonade |

There is a clue in the comments about how to implement the body of this method.
All that we'll need to do is copy the existing implementation of the `sellLemonade`
method and modify the first line to create a new `Lemonade` object using the
parameters provided instead of calling the default `Lemonade` constructor.

## Adding a Static Method to the `Lemonade` Class

The `Lemonade` class has a comment at the bottom indicating that we need to add
a static method called `mix` to the `Lemonade` class that allows us to create a
new `Lemonade`object by mixing two other `Lemonade` objects.

The `mix` method should take two parameters (in this order!):

| Parameter | Type     | Description              |
|-----------|----------|--------------------------|
| lemonade1 | Lemonade | The first `Lemonade` object to mix |
| lemonade2 | Lemonade | The second `Lemonade` object to mix |

To implement this method, we should set up variables to hold the combined
amounts of lemons, sugar, and ice from the two `Lemonade` objects, and then
create a new `Lemonade` object using these combined values to call the
`Lemonade` constructor that takes three parameters.

## Additional Challenge

If you finish and want an additional challenge, try adding yet another
overloaded version of the `sellLemonade` method that creates a default `Lemonade`
object and sells it as the normal one does, but inlcudes a parameter specifying
a percentage discount to apply to the price of the lemonade.

You will also need to modify the `Main` class to allow the user to select to 
sell a discounted lemonade and provide the discount percentage.

This is a particularly challenging exercise, that will require you to 
comprehensively understand the existing code and how the `LemonadeStand` class
works.

If you open the `LemonadeStandTest` class in the `src/test/java/org/example`
directory, you will see that there is a commented out test at the bottom that
you can use to verify your solution.  You will need to comment out this test
by removing the starting `/*` and ending `*/` lines, and then run the tests
as usual to verify your solution.
