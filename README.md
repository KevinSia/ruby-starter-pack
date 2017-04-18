# ~SAPPHIRE~ ~EMERALD~ ~DIAMOND~ ~PEARL~ 
# RUBY!
 A little history about programming.
  - https://en.wikipedia.org/wiki/History_of_programming_languages

## Let's start by expanding your programming vocablulary

### **Script**
  - A script is a plain text file containing commands/codes/instructions that you write and pass to the a program to run.
  
### **Terminal**
  - Also known as `shell`
  - The shell is a program that takes keyboard commands and passes them to the operating system to carry out. 
  - We have been using what we called GUI (Graphical User Interface)
    - It is made for people to use computers more easily/intuitively.
    - It also takes up a lot of computer resources (memory).
    - We are now learning to make websites, which essentially means we need to know how to make programs for computer to serve web pages automatically, without having a human.
    
### **Ruby**
  - It's a programming language.
  - We write codes to 'tell' the computer to do what we want. `Ruby` is one of the many languages we can use to 'communicate' with the computer
  - A human can understand a few languages:
    - I understands Chinese, English, Malay, Cantonese. You can communicate with me with those languages.
  - Whereas a computer can 'understand' many different languages (limits by how many languages are available out there, and how many language programs can you install in your computer). One will just need to install the respective program for a computer to 'understand' that language.
  
Example:

Assume a file in your computer that looks like below:
```ruby
# test.rb
5.times { puts "hello world" }
```
> The file `test.rb` contains commands in Ruby language to print `hello world` 5 times in the terminal. The `.rb` extension  is to indicate that it's a `Ruby` file. Not a `Python` file. Not a `Cobra` file.

> For the computer to 'understand' the commands in this file, one would need to install the `Ruby` program in the    computer. (the `Ruby` program can be seen as a kind of translator to the computer)

> Then to execute this file, one would just need to type `ruby test.rb` in the terminal/shell, followed by the Enter key to send this command to the operating system.
  
A Python file that contains similiar commands (print `hello world` 5 times in the terminal) may look like this
```python
for i in range(5):
  print "hello world"
```
  
A C file example:
```C
#include <stdio.h>

int main (void) {
  int i;
  for(i = 0; i < 5; i++){
    printf("hello world");
  }

  return 0;
}
```
  
The `syntax` (grammar equivalent of human language) may be different, but it's doing the same thing.

Choice of language can depend on many factors. Ruby is our choice because:
- it reads more like English, which is easier for beginners to start.
- it's a high level general purpose language (low level languages like `C` or `Assembly` languages are harder to write and requires good computer knowledge to work with.)
- it's the language behind Rails, a framework written in Ruby to build web applications.

How nice would it be if we could just 'install' a program in our brain and we can understand a language right away. (or is it not?)

### **IRB**
  - stands for _Interactive Ruby_
  - it is a program that ships along with the ruby program (meaning it comes together when you install the `ruby` program into your computer)
  - it opens up an interactive session in the terminal, allow users to execute a ruby command like executing commands in the terminal (a line of code can be executed right away by pressing enter after typing, while a script allows user to put many lines of code, and runs it in one shot)
  - it's mostly used as a playground to test/play with codes in an interactive manner. Script(s) are still needed for automation.

## Going into Ruby
### Input and Output
  - Getting user input 
    - `gets.chomp` (ever wonder what happens if you don't put `chomp`)?
  - Printing into console/terminal
    - `puts`
    - `print`
    - `p`
    
### Basic Data Types [Not complete]
- Integer
  - used for calculation (`+`, `-`, `*`, `/`, `%`)
  ```ruby
      1 + 2 # => 2
      2 - 3 # => -1
      3 * 4 # => 12
      4 / 2 # => 1
      13 / 5 # => 2 (the first digit is returned instead)
      5 % 2 # => 1 (remainder)
  ```
  - built-in methods
  ```ruby
  1.even? # => true (a boolean)
  2.odd? # => false (a boolean)
  15.round(2) # => 20
  ```
- String
  - used to represent a *string* of characters, starts and ends with double quotes(`"`) or single quotes (`'`)
  ```ruby
  "hello world"
  "foo bar baz is commonly used by programmers for placeholder texts"
  "you c@n h@v3 any k&nd of charact#rs (inside) a $tring! Even s'ngle quotes!"
  "if you want to have double quotes inside a string, use \ (backslash)"
  "like \"such\""
  ```
  - built-in methods
  ```ruby
  "shout your lungs out".upcase
  "CALM YOURSELF DOWN".downcase
  "first character should be capitalized".capitalize
  "This sentence contains fourty-five characters".length
  "melborp a regnol on si esrever ni gnidaeR".reverse
  "Subsituting the first word in word".sub("first", "second")
  "when what where".gsub('w', 't')
  ``` 
- Boolean
  - used to evaluate truthfulness in programming
  ```ruby
  # == compares two things and gives `true` if they are exactly the same
  1 == 1 # true
  "what liars say" == "what liars do" # false
  true == true # true
  true == false # false
  false == false # true

  string1 = "hello"
  string2 = "Hello"

  string1 == string2 # false

  # != compares two things and gives `true` if they are different
  1 != 2 # true
  1 != 1 # false

  true != true # false
  true != false # true
  false != false # false

  # `<`,`>`, `<=`, `>=` can be used to compare two data's relational position

  1 > 2 # true
  10 < 20 # false
  1 >= 1 # true
  10 <= 10 # true
  'n' > 'b' # true
  'z' < 'a' # false
  'A' < 'z' # true (in computer, capital letters comes before lower case letters, refer to ASCII codes to know more)

  # `&&` (AND operator)
  # takes two statements on left and right
  # evaluates to true ONLY if the two statements evaluate to true
  # else gives false

  a = 5
  a > 0 && a < 10 # (true && true) => true
  a > 0 && a < 5 # (true && false) => false
  a > 6 && a > 1 # (false && true) => false
  a > 10 && a > 20 # (false && false) => false

  # boolean values are used for if-else statements and for loops
  ```
- Array
  - access element (`[]`)
  - change element on a particular index (`[]=`)
  - taking a sub collection of elements
  - array methods (`pop`, `push`, `shift`, `unshift`, `insert`) etc.
  - string, in ruby, behaves similiarly to array when it comes to the method (`[]`/`.slice` and `[]=`)
- Hashes
  - key-value store

- Floats
  - decimal numbers
- Symbols
  - not used for normal text
  - text for internal purpose (not for printing and showing)
  - object_id
- Nil
  - to represent empty/nothing in a program
  - say if an element is not in an array, `.index` will give `nil` instead, to represent nothing is found.

### Assigning a value into a variable 
  - `my_string = 'foo bar'`
    - the lines reads: assign 'foo bar' (string) into a variable `my_string`
    - a variable is used to give a name/reference to a value. The value can then be referred back by using the variable name.
    
      ```ruby
      a_string = "hello world"
      puts a_string # hello world
      ```
    - a variable may contain different value at different point of code execution
      
      ```ruby
      a_string = "hello world"
      puts a_string # hello world
      a_string = a.string.upcase
      puts a_string # HELLO WORLD
      ```
    - a variable can (and very often)6be used to store values that comes elsewhere (eg. user input)
      ```ruby
      puts "What is your name?"
      an_input = gets.chomp
      puts an_input.capitalize
      ```
      - We will never be sure what is the value that contains inside the variable `an_input`, because it depends on user's input. If the user types `"kevin"`, the variable `an_input` will contain `"kevin"`, and the program will continue to 'capitalize' the value inside `an_input`, and finally prints it out to the terminal.
      - This program will now be able to accept input from users, and process that input accordingly.
      - Google's code to power the search bar **probably** looks like this. (okay maybe a lot more lines than this. Apparently Google has more than 2 million code to power all of it's applications. Written by a lot of programmers of course.)

## Conditional statements
  - using `if-elsif-else`
    ```ruby
    if <a-statement>
      # do something
    elsif <another-statement>
      # do something else
    else
      # do do do do do
    end
    
    a = gets.chomp
    
    if a < 5
      puts "less than 5"
    elsif a >= 5 && a < 10
      puts "more than or equals to 5 and less than 10"
    else
      puts "out of range"
    end
    
    # the following code will produce the same result as above. Try to figure out why.
    if a >= 10
      puts "out of range"
    elsif a >= 5
      puts "more than or equals to 5 and less than 10"
    else
      puts "less than 5"
    end
    
    # how you structure your `if-else` statement doesn't really matter, as long you get your desire result.
    # but if your program has a lot of `if-else` statement and 90% of the time you're sure that it will go to the `else` statement, it might boost a little performance if you refactor it
    
    # before
    if rand(1..100) < 2
      puts "99% chance"
    else
      puts "1% chance"
    end
    
    # after
    if rand(1..100) > 1
      puts "99% chance"
    else
      puts "1% chance"
    end
    
    
    ```
  - using `case-when-else`
    ```ruby
    puts "Welcome to my program. Ask me a question"
    puts "1. Why don't some couples go to the gym?"
    puts "2. Why can't a bicycle stand up on it's own?"
    puts "3. Why did the banana go to the doctor?"
    
    input = gets.chomp
    
    case input
    when "1"
      puts "Because their relationship don't *work out*"
    when "2"
      puts "Because it's *two tyred*"
    when "3"
      puts "It's not *peeling* well..."
    else
      puts "You fool!"
    end
  ```
  
## Using custom methods
  - Remember Rule #1: a method will always return data, whether its an integer, string, an array, or `nil`
  - one can use the return value of a method in several ways
  ```ruby
  # saving the data returned by a method into a variable
  result = "upcase".upcase
  
  # applying/chaining methods together
  # the result of `"never change".upcase`, which is `"NEVER CHANGE"`, will be downcased by the followed `.downcase`
  "never change".upcase.downcase.capitalize.downcase.center(20, '@')
  # chaining methods together like this is generally not a good design of code, as it can be prone to error, unless a certain guideline is met (Law of Demeter).
  # this will be talked more in OOP week
  ```
  
  - Method definition
    ```ruby
    def a_method_without_argument
      puts "Combine/package/gather related pieces of code"
      puts "And put it together under a method"
      puts "Allows you to give a name to those pieces of code"
      puts "And Ruby will know to run these codes, when it sees the name of the method"
      puts "This provides ways to organize related codes, which leads to code organization."
      puts "You probably want your code to be neat if you have a 1000 lines of code"
    end

    # to use/call/execute/run a method, just put the name of the method
    a_method_without_argument 
    ```
  - A method will always return data, whether its an integer, string, or `nil`
    ```ruby
      def method_with_keyword_return
        puts "this method returns a string 'hello' whenever it's called"
        puts "the output can then be used outside of this method for further manipulation"
        puts "a method can only return one data at a time, though not limited to any data type"
        puts "thus, one can also creata a method that returns an array"
        return 'hello'
      end
    # In the single line of code below, method_with_keyword_return will be executed first, which will execute the code inside the method
    # the `return` keyword will tell the program to return a string 'hello' back here
    # the returned string will then be upcased, and finally `puts` will do it's job.
    puts method_with_keyword_return.upcase # => outputs Hello
    ```
  - Particularly in Ruby, the `return` keyword is optional
    - If the keyword `return` doesn't exist in the method
    - Ruby will decide to return the result of the last statement in the method
    ```ruby
    def method_without_return_keyword
      puts "the last line in the method will be returned"
      puts "give it a try!"
      "hello".upcase # the string will be 'upcased' before it gets returned back
    end
    
    # Ruby will translate the method internally to something like this
    def method_without_return_keyword
      puts "the last line in the method will be returned"
      puts "give it a try!"
      return ("hello".upcase) # or `return "hello".upcase`, the bracket won't matter much in most of the cases.
    end
  
    result = method_with_keyword_return
    puts result # => outputs HELLO
    ```
  - Common mistake of a Ruby beginner
    ```ruby
    # trying to make the output of a method, one might write it this way
    def method_with_puts_last_line
      intense_calculation_result = 5 + 4 - 3 * 2 / 1
      puts intense_calculation_result
    end

    storage = method_with_puts_last_line
    storage.even? # Error! NoMethodError: undefined method `even?' for nil:NilClass
    ```
    - remember Rule #1: every method returns a data
      ```
      # the method will be translated by Ruby into something like this
      def method_with_puts_last_line
        intense_calculation_result = 5 + 4 - 3 * 2 / 1
        return (puts intense_calculation_result)
      end
      ```
    > You must know that, `puts` in ruby, is a method, rather than a keyword (`def`, `end`, `if`, `else`, `return`).
    > Having `puts intense_calculation_result` as the last line,
    > the program will first print the value inside the variable `intense_calculation_result` out to the terminal
    > then that line itself will be evaluated to `nil`
    > and since it's the last line of the method, the value `nil` will also become the return value of the method `method_with_puts_last_line`
    > which eventually get stored to the variable `storage`
  
    - A good method design pattern will be leaving the method to only do the calculations/manipulation it needs to do, and printing the result outside of the method
    ```ruby
    def method_fix
      5 + 4 - 3 * 2 / 1
    end
  
    result = method_fix
    puts result
    ```
    > this way, the result data gotten from `method_fix` can be stored into a variable, and can be further used for more.
    - Another example
    ```ruby 
    def meter_to_foot(number)
      number * 3.28084
    end

    def foot_to_inch(number)
      number * 12
    end

    result = meter_to_foot(20)
    result = foot_to_inch(result)
    
    puts result
    ```
   - But of course, if your method is designed to not return anything back, its completely fine for the last line to have `puts`.
    ```ruby
    def main_menu
      puts "Hello. I'm Seeree! What do you want me to do?"
      puts "1. Turn on the lights"
      puts "2. Turn off the lights"
    end

    main_menu
    input = gets.chomp
    case input
    when "1"
      puts "I have turn on the lights"
    when "2"
      puts "I have turn off the lights"
    else
      puts "I don't understand what are you trying to say"
    end
    ```
    
  > If you could not understand above in 2 minutes (or give yourself a time frame), please move on. 
  > Sometimes people learn and remember only when mistakes are made, and in the programming world, mistakes/errors are always made, and it's perfectly fine and safe to make (at least for now, since this is a development environment. 
  > Programmers will very often need a safe environment, often called the development environment to be able to code without having to worry of making code mistakes. Just like how there are test drive fields for car manufacturers and labs for scientists). 
  
  (not if you repeat those mistakes, again and again, just like anything in life. I guess?)
    
  ### let's go on shall we?

  A method cant be very useful if we can package code, but not flexible enough for a small part of it to be changed given some input, right?
  ```ruby
  def a_method_with_argument(argument1)
    puts "argument1 here acts like a placeholder"
    puts "the program can call this method along with an argument as below"
    puts "a_method_with_argument('a string')"
    puts "argument1 can be used like a normal variable inside the method, and can only be used inside the method"
    puts "argument1 = #{argument1}"
  end
  
  a_method_with_argument("hello")
  ```
  
  A method can also accept any number of arguments stated in the definition, doesn't matter if they are used inside the method or not
  ```ruby
  def method_with_5_arguments(a1, a2, a3, a4, a5)
    a1 + a2
  end
  
  # ArgumentError!
  method_with_5_arguments(1,2,3,4) 
  ```
  > A method call must supply the number of arguments stated in the method definition, which is 5 in this case (a1, a2, a3, a4, a5). Any number of arguments that is not 5 will cause Ruby to raise an ArgumentError.
  ```ruby
  method_with_5_arguments(1,2,3,4,5) # => 3
  ```
  
  Though, an argument can have a default
  ```ruby
  def excited(word, number = 1)
    word + "!" * number
  end
  
  excited("coding") # => "coding!" (one argument, second argument default to 1)
  excited("coding", 15) # => "coding!!!!!!!!!!!!!!" (two argument, second argument becomes 10, default is not used)
  ```
  > By the way, if you counted the number of exclaimation marks above, you will notice there are only 14 "!". That proves you're sharp! Being sharp as a programmer can certainly help you a lot on improving yourself! Well if you don't, mmmmmmmmaybe it's time to train your attention to details.



- String
  - built-in methods 
    - `.upcase`, `.capitalize`, `.swapcase`, etc
    - `.length`, `.index`, `.start_with?`, etc.
    - `.slice`, `.slice!`, etc.
  - string interpolation  
    ```ruby
    puts "What is your age?"
    input = gets.chomp.to_i # to integer
    puts "Your age is #{input + 10}!"
    ```
    
