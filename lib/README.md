# Magazine Article Tracker
This is a simple Ruby project that allows you to track articles and authors for various magazines. It includes three classes: Author, Magazine, and Article.


## How to Use
Once you've run the run.rb file in the lib folder *(ruby bin/run.rb)*, you can interact with the code by following the prompts in the terminal. The code includes the following classes and methods:




### Magazine
initialize(name, category): Creates a new magazine with the given name and category.

name: Returns the name of the magazine.

category: Returns the category of the magazine.

all: Returns an array of all the magazines that have been created.

find_by_name(name): Returns the first magazine object that matches the given name.

article_titles: Returns an array of all the article titles for the magazine.

contributors: Returns an array of all the authors who have written for the magazine.

#### BDD
Given a Magazine with a name and category,
When I call the `name` method,
Then it should return the name of the Magazine.

Given a Magazine with a name and category,
When I call the `category` method,
Then it should return the category of the Magazine.

Given a Magazine with a name and category,
When I call the `name=` method with a new name,
Then it should update the name of the Magazine.

Given a Magazine with a name and category,
When I call the `category=` method with a new category,
Then it should update the category of the Magazine.

Given a list of Magazine instances,
When I call the `all` method,
Then it should return an array of all Magazine instances.

Given a list of Magazine instances and a name,
When I call the `find_by_name` method,
Then it should return the first magazine object that matches the name.

Given a Magazine with a list of Article instances,
When I call the `article_titles` method,
Then it should return an array string of the titles of

#### Pseudo Code
class Magazine
  def initialize(name, category)
    @name = name
    @category = category
  end

  def name
    @name
  end

  def category
    @category
  end

  def name=(name)
    @name = name
  end

  def category=(category)
    @category = category
  end

  def self.all
    # returns an array of all Magazine instances
  end

  def self.find_by_name(name)
    # returns the first magazine object that matches the name
  end

  def article_titles
    # returns an array of the titles of all articles written for that magazine
  end

  def contributing_authors
    # returns an array of authors who have written more than 2 articles for the magazine
  end

  def contributors
    # returns an array of Author instances who have written for this magazine
  end
end

### Author
initialize(name): Creates a new author with the given name.

name: Returns the name of the author.

articles: Returns an array of all the articles written by the author.

magazines: Returns a unique array of all the magazines the author has contributed to.

add_article(magazine, title): Creates a new article with the given title and associates it with the author and the given magazine.

topic_areas: Returns a unique array of all the topic areas the author has written about.

#### BDD
Given an Author with a name,
When I call the `name` method,
Then it should return the name of the Author.

Given an Author with a list of Article instances,
When I call the `articles` method,
Then it should return an array of Article instances the author has written.

Given an Author with a list of Article instances,
When I call the `magazines` method,
Then it should return a unique array of Magazine instances for which the author has contributed to.

Given an Author,
When I call the `add_article` method with a magazine instance and a title,
Then it should create a new Article instance and associate it with the author and the magazine.

Given an Author with a list of Article instances,
When I call the `topic_areas` method,
Then it should return a unique array of strings with the categories of the magazines the author has contributed to.


#### Pseudo Code
class Author
  def initialize(name)
    @name = name
  end

  def name
    @name
  end

  def articles
    # returns an array of Article instances the author has written
  end

  def magazines
    # returns a unique array of Magazine instances for which the author has contributed to
  end

  def add_article(magazine, title)
    # creates a new Article instance and associates it with that author and that magazine
  end

  def topic_areas
    # returns a unique array of strings with the categories of the magazines the author has contributed to
  end
end

### Article
initialize(author, magazine, title): Creates a new article with the given author, magazine, and title.

title: Returns the title of the article.

all: Returns an array of all the articles that have been created.

author: Returns the author of the article.

magazine: Returns the magazine of the article.

#### BDD
Author.new(name) takes a string name and returns an instance of Author with the name instance variable set to name.

Author#name returns the name instance variable.

Author#articles returns an array of all Article instances that have this author as their author.

Author#magazines returns a unique array of Magazine instances that this author has contributed to.

Author#add_article(magazine, title) takes a Magazine instance and a string title, creates a new Article instance with this author, the given magazine, and the given title, and returns the new Article instance.

Author#topic_areas returns a unique array of category strings for Magazine instances that this author has contributed to.

#### Pseudo code
class Magazine
  @@all = []

  def initialize(name, category)
    # set name and category instance variables
    # add this instance to @@all
  end

  def self.all
    # return @@all array
  end

  def name
    # return name instance variable
  end

  def category
    # return category instance variable
  end

  def name=(new_name)
    # set name instance variable to new_name
  end

  def category=(new_category)
    # set category instance variable to new_category
  end

  def contributors
    # return array of authors who have written for this magazine
  end

  def self.find_by_name(name)
    # return first magazine instance with matching name
  end

  def article_titles
    # return array of article titles for this magazine
  end

  def contributing_authors
    # return array of authors who have written more than 2 articles for this magazine
  end
end




## License
This project is licensed under the MIT License. Feel free to use and modify this code for your own purposes.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
Copyright (c) 2023 **Isaac ongera**








