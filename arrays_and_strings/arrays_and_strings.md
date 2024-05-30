# Arrays and strings

In terms of algorithm problems, arrays (1D) and strings are very similar: they both represent an ordered group of elements.
Most algorithm problems will include either an array or string as part of the input, so it's important to be comfortable
with the basic operations and to learn the most common patterns.

"Array" can mean something different between languages. For example, Python primarily uses "lists" instead of arrays which
are extremely lenient. Initialization is as easy as `arr = []`, and you don't need to worry about the type of data you store
in the list or the size of the list. Other languages like C++ require you to specify the size and data type of the array 
during initialization, but also have support for lists (like `std::vector` in C++).

> Technically, an array can't be resized. A dynamic array, or list, can be. In the context of algorithm problems, usually
> when people talk about arrays, they are referring to dynamic arrays.

Similarly, strings are implemented differently between languages. In Python and Java, they are immutable. In C++, they are
mutable. It's important to know the details behind arrays and strings for the language you plan on using in interviews.

> Mutable: a type of data that can be changed. 
> Immutable: a type of data that cannot be changed.
> If you want to change something immutable, you will need to recreate the entire thing.

Why should we care about something being mutable of immutable? If you have a mutable array `arr = ["a", "b", "c"]` and an
immutable string `s = "abc"`, but you want to instead represent `"abd"`, you can easily do `arr[2] = "d"`, but you cannot
do `s[2] = "d"`. As such, if you wanted the string `s = "abd"`, you would need to create it entirely from scratch. With such
a small string, it's not a big deal. But sometimes you are dealing with strings with 100,000 characters, so creating new
versions just to modify one character is very expensive (*O(n)*, where *n* is the size of the string).

As I mentioned before, a majority pf algorithm problems will involve an array or string. They are extremely versatile data
structures and it's impossible to list all the relevant problem-solving techniques in one article. In the next few articles,
we'll go over the most common techniques. But first, let's take a quick look at the complexity of array and string operations.

| Operation | Array\List | String(Immutable) |
| --- |------------|-------------------|
| Appending to end | *O(1)*     | *O(n)*            |
| Popping from end | *O(1)*     | *O(n)*            |
| Insertion, not from end | *O(n)*     | *O(n)*            |
| Deletion, not from end | *O(n)*     | *O(n)*            |
| Modifying an element | *O(1)*     | *O(n)*            |
| Random access | *O(1)*     | *O(1)*            |
| Checking if element exists | *O(n)* |*O(n)* |

> Appending to the end of a list is [amortized *O(1)*](https://stackoverflow.com/questions/33044883/why-is-the-time-complexity-of-pythons-list-append-method-o1)