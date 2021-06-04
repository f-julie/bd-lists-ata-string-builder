## ATAStringBuilder

**Branch name:** lists-classroom

**RDE workflow:** 
* lists-string-builder-completion
* lists-string-builder-extension-one
* lists-string-builder-extension-two

This activity will provide you with practice interacting with the List 
interface. We will be building our own String builder. Remember, that
more efficient way to concatenate `String`s? It's your turn to try 
your hand at building one. 

Open up the class `ATAStringBuilder` located in this package. 

### Internal State
We will be keeping a track of all the characters in our string builder
in a `List`. You should see a private `List` of `Character`s called 
`value` at the top of the class. This is the field you will append to, 
insert into, search through, and remove from. 

### Constructors
Let's start by implementing the constructors. We will need to initialize
our Lists. What's a concrete implementation of List that we've learned 
about that we can instantiate here? In our no args constructor we just
need to instantiate a new list. In the constructor where we accept an
initial string value, we will also need to append that information to 
the list. Can we use a method of the class to do this?

### Completion
We will be implementing the below methods for completion. There are
unit tests in the class `ATAStringBuilderCompletionTests` so that you
can validate the code you have written. You can run these from IntelliJ 
or using the rde workflow:

`lists-string-builder-completion`

Each of the following methods have Javadocs in the class for you to 
learn about the methods behavior.

#### `int length()`

#### `ATAStringBuilder append(String str)`
This method returns an ATAStringBuilder, more specifically it returns the
object you are calling the method on. This is a unique pattern that we
have seen in our project. For example, the Order class has a Builder class
that does this too. It allows you to chain together method calls. This is
an example of a **fluid API**.

The intended use is:

```
    ATAStringBuilder sb = new ATAStringBuilder();
    sb.append("ATA ")
        .append("v2 ")
        .append("rulez");
```

In order to return the object you are currently working with, you can do
the following:

`return this;`

**HINT:** The String method [valueOf](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#valueOf(java.lang.Object)) 
may be helpful here.

#### `ATAStringBuilder insert(int offset, char c)`
Again, this returns an object of type `ATAStringBuilder`, specifically 
the object you are manipulating. Use the return statement suggested above.

#### `char charAt(int index)`

### Completion Goal
* Implemented the following methods in `ATAStringBuilder`
  * `int length()`
  * `ATAStringBuilder append(String str)`
  * `ATAStringBuilder insert(int offset, char c`
  * `char charAt(int index)`
* Workflow `lists-string-builder-completion` succeeds

### Extension One
Implement the methods below that let you manipulate specific characters:

#### `ATAStringBuilder setCharAt(int index, char ch)`
#### `ATAStringBuilder deleteCharAt(int index)`

There are unit tests in the class `ATAStringBuilderExtensionOneTests` so
that you can validate the code you have written. You can run these from
IntelliJ or using the rde workflow:

`lists-string-builder-extension-one`

### Extension Two
Implement the methods below:

#### `ATAStringBuilder append(Object obj)`
#### `ATAStringBuilder insert(int offset, String str)`
#### `String substring(int start, int end)`

There are unit tests in the class `ATAStringBuilderExtensionTwoTests` so
that you can validate the code you have written. You can run these from
IntelliJ or using the rde workflow:

`lists-string-builder-extension-two`

### Commit & Push

1. When you have the code to where you want it (at least compiling, ideally all
   tests passing), commit it.
1. Push it to your remote branch.
3. Go back to the ATAStringBuilder Canvas page and paste in a link to your commit on
   Code Browser.
