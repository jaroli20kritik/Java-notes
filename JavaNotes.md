>### 20.07.2020

+ Visual Studio Code 
+ Working in Markdown
   > + HEADERS
   > BLOCKQUOTES
   > As Grace Hopper said:
   > > I’ve always been more interested
   > > in the future than in the past.
   >  As Grace Hopper said:
   >  I've always been more interested
   >  in the future than in the past.
   > MARKDOWN
   > SYNTA X
   > IMAGES
   > ![GitHub Logo](/images/logo.png)
   > Format: ![Alt Text](url)
   > LINKS
   > http://github.com - automatic!
   > [GitHub](http://github.com)
   > Unordered
   > 1. Item 1
   > 2. Item 2
   > 3. Item 3
   > * Item 3a
   > * Item 3b
   > Ordered
   > BACKSLASH ESCAPES
   > Markdown allows you to use backslash escapes to generate literal characters which
   > would otherwise have special meaning in Markdown’s formaing syntax.
   > Markdown provides backslash escapes for
   > the following characters:
   > \ backslash
   > ` backtick
   > * asterisk
   > _ underscore
   > {} curly braces
   > [] square brackets
   > () parentheses
   > ##### hash mark
   > + plus sign
   > - minus sign (hyphen)
   > . dot
   > ! exclamation



+ How to write notes in Markdown?

>### 21.07.2020

+ Woking with Intellij IDEA and it's shortcuts
+ Introduction to Github
+ Set keymap as eclipse

>### 22.07.2020

+ #### Concept of Packages
    + Package in Java is a mechanism to encapsulate a group of classes, sub packages and interfaces.
    + Preventing naming conflicts. For example there can be two classes with name Employee in two packages, college.staff.cse.Employee and college.staff.ee.Employee
    + Making searching/locating and usage of classes, interfaces, enumerations and annotations easier
    + Providing controlled access: protected and default have package level access control. A protected member is accessible by classes in the same package and its subclasses. A default member (without any access specifier) is accessible by classes in the same package only.
    + Packages can be considered as data encapsulation (or data-hiding).
    + Package names and directory structure are closely related. For example if a package name is college.staff.cse, then there are three directories, college, staff and cse such that cse is present in staff and staff is present college.
+ #### Concept of import statements
    + In Java, the import statement is used to bring certain classes or the entire packages, into visibility. As soon as imported, a class can be referred to directly by using only its name.

    + The import statement is a convenience to the programmer and is not technically needed to write complete Java program

+ #### Difference between reference and objects
    +   The objects are created in the heap area and, the   reference obj just points out to the object of the      Student class in the heap, i.e. it just holds the memory address of the object (in the heap).
    
        And since the String is also an object, under name, a reference points out to the actual String value (“Krishna”).

        In short, object is an instance of a class and reference (variable) points out to the object created in the heap area.
+ #### Concept of static method
    + Static Method in Java belongs to the class and not its instances. A static method can access only static variables of class and invoke only static methods of the class.

    + Usually, static methods are utility methods that we want to expose to be used by other classes without the need of creating an instance. For example Collections class.

    + Java Wrapper classes and utility classes contain a lot of static methods. The main() method that is the entry point of a java program itself is a static method.

>### 04.08.2020

+ Concept of companion class
+ collections <E>
    + It means that you're dealing with a collection of items with type E. Imagine you've got a cup of tea. Instead of tea, it could also hold coffee so it makes sense to describe the cup as a generic entity:

    + class Cup<T> { … }
    + now you could fill it, either with coffee or tea (or something else):

    + Cup<Tea> cuppa = new Cup<Tea>();
    + Cup<Coffee> foamee = new Cup<Coffee>();
+ default stream
    +  the Stream API is used to process collections of objects. A stream is a sequence of objects that supports various methods which can be pipelined to produce the desired result.
    + The features of Java stream are –

        + A stream is not a data structure instead it takes input from the Collections, Arrays or I/O channels.
        + Streams don’t change the original data structure, they only provide the result as per the pipelined methods.
        + Each intermediate operation is lazily executed and returns a stream as a result, hence various intermediate operations can be pipelined. Terminal operations mark the end of the stream and return the result.
    + Different Operations On Streams-
        + Intermediate Operations:

            1. map: The map method is used to returns a stream consisting of the results of applying the given function to the elements of this stream.
            List number = Arrays.asList(2,3,4,5);
            List square = number.stream().map(x->x*x).collect(Collectors.toList());
            2. filter: The filter method is used to select elements as per the Predicate passed as argument.
            List names = Arrays.asList("Reflection","Collection","Stream");
            List result = names.stream().filter(s->s.startsWith("S")).collect(Collectors.toList());
            3. sorted: The sorted method is used to sort the stream.
            List names = Arrays.asList("Reflection","Collection","Stream");
            List result = names.stream().sorted().collect(Collectors.toList());
        + Terminal Operations:

            1. collect: The collect method is used to return the result of the intermediate operations performed on the stream.
            List number = Arrays.asList(2,3,4,5,3);
            Set square = number.stream().map(x->x*x).collect(Collectors.toSet());
            2. forEach: The forEach method is used to iterate through every element of the stream.
            List number = Arrays.asList(2,3,4,5);
            number.stream().map(x->x*x).forEach(y->System.out.println(y));
            3. reduce: The reduce method is used to reduce the elements of a stream to a single value.
            The reduce method takes a BinaryOperator as a parameter.
            List number = Arrays.asList(2,3,4,5);
            int even = number.stream().filter(x->x%2==0).reduce(0,(ans,i)-> ans+i);
+ Terminal methods (Does not return stream) .filter()
+ Non-terminal methods (Returns stream) .filter()
+ Optional class 
    + Optional is a container object used to contain not-null objects. Optional object is used to represent null with absent value. This class has various utility methods to facilitate code to handle values as ‘available’ or ‘not available’ instead of checking null values.
    + Following is the declaration for java.util.Optional<T> class −

    >public final class Optional<> extends Object
+ concept of .flatMap()
    + Stream flatMap(Function mapper) returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Stream flatMap(Function mapper) is an intermediate operation. These operations are always lazy. Intermediate operations are invoked on a Stream instance and after they finish their processing, they give a Stream instance as output.


>### 05.08.2020

+ Difference between statement and expression
    + b + 1 is an expression while a = b + 1; is a statement. A statement consists of expressions.

    + This is not specific to the Java language. Many languages use this kind of grammar e.g. C, C++, Basic etc (not SQL).
+ Anonymous inner class concept
    + It is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain “extras” such as overloading methods of a class or interface, without having to actually subclass a class.
+ Concept of predicate
	+ Predicate <Integer> isEven = new Predicate <Integer>() {
	 	.
		.
		.         Predicate returns boolean value
		.
		.
	}
+ Concept of Runnable()
    + java.lang.Runnable is an interface that is to be implemented by a class whose instances are intended to be executed by a thread. There are two ways to start a new Thread – Subclass Thread and implement Runnable. There is no need of subclassing Thread when a task can be done by overriding only run() method of Runnable.
+ External Iterator and Internal Iterator
+ Method Reference (::)
+ Concept Lambda Expressions 
    + Lambda expressions are introduced in Java 8 and are touted to be the biggest feature of Java 8. Lambda expression facilitates functional programming, and simplifies the development a lot.

    + Syntax
    A lambda expression is characterized by the following syntax.

    >parameter -> expression body

    + Following are the important characteristics of a lambda expression.

        + Optional type declaration − No need to declare the type of a parameter. The compiler can inference the same from the value of the parameter.

        + Optional parenthesis around parameter − No need to declare a single parameter in parenthesis. For multiple parameters, parentheses are required.

        + Optional curly braces − No need to use curly braces in expression body if the body contains a single statement.

        + Optional return keyword − The compiler automatically returns the value if the body has a single expression to return the value. Curly braces are required to indicate that expression returns a value.



