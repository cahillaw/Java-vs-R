## Some Differences Between Java and R
# Andy Cahill


Before I learned R, the only programming language I knew was Java. So when I started learning R, I naturally started
comparing the similarities and differences between the languages. For the most part, R came pretty easily to me because
there were alot of similarities in the basics. For example, to create a variables `int x = 4;` in Java was `x <- 4` in R, 
Methods (functions in R) worked very similarly despite different notation: `public int add (int x, int y) { return x + y; }`
in Java became `add <- function(x,y) {x+y}` in R.

The trend between the differences was how R code did more things for you (like the variable types) and was shorter overall.
The next thing to look at was the backbone of Java programming, for loops. Again, in both languages, they are very similar, 
with the Java syntax being `for(int i = 0; i < 10; i++) {System.out.println(i);}` while R's syntax was `for(i in c(0:9)) {print(i)}`
When I first learned R, I assumed I would be using for loops regularly, just like I did in Java, however I couldn't be more wrong.

That is because of the concept of vectorized operations, a concept that does not exist in Java.

I think vectorized operations are best explained with an example, so here is an example in its most basic form. Imagine we have set
a R vector like this `x <- 1:10` and we want to add 1 to every element in the vector. In Java, the easiest way of doing this is a for 
loop that looks a little like this: `for(int i = 0; i<10; i++) {x[i] = x[i+1]; }` Basically, this is looping over all of the elements 
in the vector (array in Java) and adding 1 to the current value. This doesn't look complex, however as you do more  things inside of
the for loop, it can get lengthy fast. You can this in R as well, however there is a much simpler way: the vectorized operations
I mentioned above.

Anyways, lets get back to R. How can we do this in R without using a for loop? Well it looks like this:
`y = x + 1`
Wait, how could it be just one line? Well R is smart enough to figure out that you have a vector, and instead of erroring out when you add
a integer to a list like it would in Java, it realizes that you are trying to add 1 to *each* value, and simply does that. To confirm this works,
try it yourself. Let the vector `x <- 1:10` and then running the code and typing y, the result should look as follows:

`[1] 2 3 4 5 6 7 8 9 10 11`

Of course, this is just a simple example that just scratches the surface of what you can do with vectorized operations. From editing data columns with
1 line of code to comparing each value in a list to a predetermined value, there is so much you can do with vectorized operations.

A second thing that R can do much easier to than Java is reading files.

In Java, if you want to read a file, you must use a Scanner, and then individually parse each line or token to get the contents and then transfer to an 
Array or other data structure to store the data. I'm not going to write out the code because it gets complicated, but this is basically what you
must do. When I started learning R, I assumed we would have to use a similar process, but again I was wrong with how easy-to-use R is. In R there 
are many built-in functions, and there are many that help read files such as `read.table()` and `read.csv()` All it takes is a single line of code:

`read.table("data.csv", sep = ",")`

There are many other parameters such as row.names and stringsAsFactors which one may want to use, but the base functionality is as written above.

In conclusion, these are only a few differences between Java and R, but already it should be easy to see how R is a data science language and
Java is not. Reading and modifying data are one line operations in R, while doing the same in Java would need quite a few. R really isn't that hard
to learn, so if you are considering making a Java program reading or creating files or using many for loops, it might be easier to learn the basics of
R and write it much more concisely.

Thats all I have for today, thank you for reading!


