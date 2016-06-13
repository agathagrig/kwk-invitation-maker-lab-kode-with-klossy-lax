

## Met Gala Invitation Maker

<img src="https://s3.amazonaws.com/after-school-assets/weasley.jpg" width="150" align="left" hspace="10">

The Met Gala is rapidly approaching and that means invitations have to go out as soon as possible! Celebrities are eagerly waiting to see if they'll get the invite - who will be on the guest list for this year's hottest event?

Currently, each invitation is being painstakingly created by hand. How can you automate this task? There are a few ways we can do this...

#### gsub
The `.gsub` method is a handy Ruby tool that allows you to `globally substitute` a word or letter for another word or letter within a string. That means *every time the word or letter appears in the string, it will be substituted out.* Let's take a look at how that works.

We have a fact about Karlie assigned to a variable `wrong_fact`:

```ruby
wrong_fact = "Karlie was born in Kansas City, Missouri"
```
But wait, Karlie is from St. Louis, not Kansas City! Let's swap out the words "Kansas City" for "St. Louis" using the gsub method. `gsub` takes two `parameters`. *The first one is the word you want to replace, and the second one is the word you want to replace it with*:

```ruby
right_fact = wrong_fact.gsub("Kansas City", "St. Louis")

=>  "Karlie was born in St. Louis, Missouri"
```

The `return value` (aka what this action produces after it's called) will be "Karlie was born in St. Louis, Missouri" Then, if we type `right_fact` into our console, we'll see the fact correctly printed.

### Chaining gsubs

What if you have a sentence that you want to substitute more than one word in? We can do that by calling `gsub` more than once on the same line, through a process called `method chaining` in which you *call one method right after another*. Take a look:

```ruby
wrong_fact = "Karlie has 5 brothers."
true_fact = wrong_fact.gsub("brothers", "sisters").gsub("5", "3")

=> "Karlie has 3 siblings"
```
### String Interpolation

There's another way to do this substitution called `string interpolation`. `String interpolation` allows us to *set a placeholder inside a string where Ruby code can be run*. We wrap whatever we want to interpolate #{inside this notation}. Oftentimes, we'll be interpolating variable names within strings.

Let's say you have this string about Karlie's recent TV appearance:

"In May, Karlie was on #{name_of_show} with #{show_host}!"

Then you make `name_of_show` a variable, and assign it to the string to be put in:

```ruby
name_of_show = "The Tonight Show"
show_host = "Jimmy Fallon"
puts "In May, Karlie was on #{name_of_show} with #{show_host}!"

=> "In May, Karlie was on The Tonight Show with Jimmy Fallow!"

```

Note that here we're declaring the variables `name_of_show` and `show_host` **before** we call `puts`. We need to do it in this order because the computer reads our program sequentially. When our computer gets to `#{name_of_show}`, it won't know what that is if `name_of_show` isn't declared yet.

Some Rubyists write this another way (we call this string concatenation):

```ruby
name_of_show = "The Tonight Show"
show_host = "Jimmy Fallon"

puts "In May, Karlie was on " + name_of_show + " with " + show_host +"!"
```
But personally, we think the first way looks nicer and is easier for your fellow programmers to read.

### Challenge 1 (using gsub):
Open the file called `invitation.rb` in your text editor.

**NOTE:** This lab does not have tests, so the learn command won't work. Instead, just write your code and test it out manually by running `ruby invitation.rb` in the command line. If the output looks like it's intended to, you're good to go and can use `learn submit` to submit your work!

Copy the variable definition below, which is the  invitation that was used for the Museum of Modern Art's fundraiser last year, and paste it into `invitation.rb`. 

```ruby
gala_invitation = "The Museum of Modern Art invites you to their annual gala on Sunday the 22nd of May 2015. Festivities will be held at the MoMA at 11 W 53rd St, New York, NY 10019
. See you then!"
```

The Met plans to use this invitation but update it to the correct data. Instead of the Museum of Modern art, the gala takes place at **The Metropolitan Museum**. The gala will take place on Saturday May 13th, 2017. In `invitation.rb` use `.gsub`s to customize the original invitation. Remember to use `puts` to output your solution to the screen.

### Challenge 2 (using string interpolation):
It's 1998 and time for Ginny's graduation. Ron wants to help his little sis out. Instead of using gsub, let's use string interpolation to change the content of the invitation. In your text editor, open the file called `ginny_invitation.rb`. You'll code your solution in that file.

Copy Percy's invitation into ginny_invitation.rb again.

```ruby
invitation = "The family of Percy Weasley proudly invite you to their graduation commencement on Saturday the 22nd of May 1993. Festivities will be held at The Burrow. See you then!"
```

Now that you know what string interpolation is, assign the following content from Percy's invitation to variables in `ginny_invitation.rb`:

1. name, 'Percy'
2. the day, 'Saturday'
3. the date, '22nd'
4. the year, '1993' 

Now that we have Percy's information, it's time to change the value of these variables to reflect Ginny's info. Ginny plans to have her party on May 17th, 1998 (Sunday).

Use string interpolation and the variables you just created to customize Percy's invitation for Ginny. As in Challenge 1, you'll want to use puts to print out your solution to the screen.

### S-T-R-E-T-C-H Challenges!
If you've made this far, here are some additional challenges for you to complete:

1.  What if Ginny wants to put her name and day of her graduation IN ALL CAPS.  How can you do this?
2.  Now that her name and day are in all caps she decides she doesn't like it and only wants to capitalize the first letter.  How can you do this?
3.  Next she doesn't want her date and day to be strings.  She wants to turn them into numbers.  Can you fix this for her?

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-invitation-maker-lab' title='Graduation Invitation Maker'>Graduation Invitation Maker</a> on Learn.co and start learning to code for free.</p>

<p class='util--hide'>View <a href='https://learn.co/lessons/hs-invitation-maker-lab'>Pre-College Lab: Invitation maker</a> on Learn.co and start learning to code for free.</p>
