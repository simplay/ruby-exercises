# Exercises

Given are the numbers from 1 to 10, i.e.
```ruby
numbers = (1..10).to_a
```

Use so called `higher order functions` to solve the following tasks:

**a)** Print each value of `numbers`.

**b)** Select all even numbers and multiply the resulting numbers by 3.

**c)** compute the sum of its squared numbers, i.e. `1^2 + 2^2 + 3^2 + ... + 10^2`

**Bonus**: Write for each task (a-c) a function that accepts an array.

**d)** Implement the following function:
```ruby

# @example
#   compute_average(array: [2,4]) #=> 3
#   compute_average(array: [3,5,10]) #=> 6
# @param array [Array] input numbers
# @return [Float] the average of the given array
def compute_average(array: )
  # TODO: your implementation goes here
end
```
**e)** Write a ruby script that asks a user to enter some whitespace separated numbers.
These numbers are used as an input of the function `#compute_average`.
The resulting average value should be displayed to the user.
Note: The user input is a string (i.e. the whitespace separated numbers). Transform them to an array of numbers using `String`'s the `split` method.

**Bonus**: The program shouldn't terminate after its first run. It rather should ask the user whether or not he wants to continue.
In case he wants to continue, repeat the program-flow, otherwise terminate the execution.

**f)** In this task you are going to solve some tasks that address text matching. To solve this task, please use the following array of names:

```ruby
names = [
  "Hans",
  "Peter",
  "Simon",
  "Sandra",
  "Petra",
  "Kristen"
]
```

Write a method that finds all names that start with a certain letter.

E.g. `find_by_letter(letter: 's')` should return ["Simon", "Sandra"] but
`find_by_letter(letter: 'x')` should return an empty array.

**g)** Generalize this function to return all names that match a certain substring

E.g. `find_by_pattern(pattern: "sa")` should return ["Sandra"] and
`find_by_pattern(pattern: "en")` should return ["Kristen"]

**h)** Count occurrence of every word in the given random text. Print the top 5 words (sorted in a descending order).

Hint 1: Make use of `group_by`, `map` to compute the word frequency (i.e. the number of occurrences per word).

Example: `a man in a house` will find the following frequencies:
`[["a", 2], ["man", 1], ["in", 1], ["house", 1]]` with the top word "a", which occurs twice.

Implement the missing code in the file `ex_array_h.rb`

```ruby
random_text = File.read("random_text.txt")
words = random_text.join
# your implementation goes here
```
**Bonus**: Save the resulting top-5 results in a text file using ruby.

Hint: Make use of the class `File`.

**i)** In this task you are going to implement a function that appends an article to a list of articles. Articles have a name and price.
See the code below and address / solve the TODOs.

```ruby
articles = []

# This method should append a new article hash to the articles array.
# An article hash keys :name and :price.
#
# @param name [String] article name, e.g. "carrots"
# @param price [Float] price of the article, e.g. 100.2
def append_article(name:, price:)
  # TODO: your implementation goes here
end

append_article(name: "shoes", price: 78.5)
append_article(name: "socks", price: 7.9)
append_article(name: "book", price: 20)
append_article(name: "apple", price: 0.65)

# articles.count #=> 4
puts articles.count

# this should print the name of the 2nd article
second_article = articles[1]
puts second_article[:name]

# TODO print the price of the 3rd article

# TODO print all articles

```

**Bonus**: Instead of using hashes, implement a class `Article` that stores the name and price of an article. Change the previous code to append `Article` instances.
Don't forget to define corresponding getters.

Example: With your implementation someone should be able to define a new article the following way:

```ruby
article = Article.new(name: "carrot", price: 2.3)
article.name #=> "carrot"
article.price #=> "2.3"
```
