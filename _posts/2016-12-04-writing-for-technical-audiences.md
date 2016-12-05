---
layout: paper
title: "Writing for Technical Audiences"
category: [Writing]
tags: [community, devrel, devangelism, writing, technical writing]
---

The approach writers take to create technical documentation differs from that of creative writing pieces. Creative writing is written to take the reader away to an imaginary world, while technical writing is focused on helping the reader solve a problem. As a result, we don't have the luxury of using lots of words to convey our ideas -- our readers want to solve a problem they're having and our goal is to help them resolve problems fast.

Outlining technical pieces happens much the same way as with creative pieces. Generally you will need a title, an introduction, a procedural list of steps the reader must take in order to reach their goal, and a conclusion that summarizes what was done. As you write technical pieces, remember that we're trying to get the reader to a solution as fast as we can without sacrificing clarity. Let's look at some steps we can take to write stronger technical documentation.

## Introduce Your Solution

Your title and your introductory paragraph work together to tell the reader two things: 1) the outcome of the article, 2) the problem this outcome solves.

Example: Your readers are trying to host websites on Ubuntu 14.04, and the solution is to set up a LAMP (Linux, Apache, MySQL, PHP) stack. You might produce something like this:

```
Title: Set Up a LAMP Stack on Ubuntu 14.04

Setting up a LAMP (Linux, Apache, MySQL, PHP) stack will allow you to host websites on Ubuntu 14.04. [...]
```

The title and introductory paragraph tell readers the outcome of the article (a LAMP stack running on Ubuntu 14.04) and what problem it solves (allowing them to host a website). However, the reader has to open the article to see what a LAMP stack is and why it might pertain to them. This is great for page views, but weak for usability.

Let's combine these to make a stronger title:

```
Title: Host Websites with a LAMP Stack on Ubuntu 14.04

Setting up a LAMP (Linux, Apache, MySQL, PHP) stack will allow you to host websites on Ubuntu 14.04. [...]
```

Better, but we can simplify this even further by removing the acronym.

```
Title: Host Websites on Ubuntu 14.04

Setting up a LAMP (Linux, Apache, MySQL, PHP) stack will allow you to host websites on Ubuntu 14.04. [...]
```

The reader wants to host a website on Ubuntu 14.04 and this title gives them enough information to decide if this guide is likely to help them. The introductory paragraph explains what will be used to solve the problem and immediately reaffirms that the reader is in the right place if they are looking to host a website on Ubuntu 14.04.

What if our organization's documentation strategy includes acquiring new customers and SEO?

```
Title: Host Websites on Ubuntu 14.04 with LAMP 

Setting up a LAMP (Linux, Apache, MySQL, PHP) stack will allow you to host websites on Ubuntu 14.04. [...]
```

This isn't ideal as we've added the acronym back into the title. However, our title still tells the reader that this guide is likely to help them solve their problem even if they're not sure what "LAMP" means. The introduction immediately defines "LAMP" and restates the problem they're trying to solve.

We could also do this another way:

```
Title: Host Websites on Ubuntu 14.04 with LAMP (Linux, Apache, MySQL, PHP)

Setting up a LAMP stack will allow you to host websites on Ubuntu 14.04. [...]
```

This isn't elegant, but it explains the acronym for the reader while giving search engines some keywords. It also gives the readers detailed information about the problem to be solved and the tools used to achieve the solution.

**Note:** As a matter of preference, I will sacrifice Google ranks for usability every time -- I would rather add overhead to my day by linking the same doc 4 times an hour than have people organically land on a document that confuses them. I can usually find a happy medium.

## Enough with the Jargon

Stop using jargon and acronyms. Many technical readers will understand "HTTP" and "API," but terms such as "MVP" are ambiguous even in technical writing. Do you mean "Most Valuable Player" or "Minimum Viable Product?" Maybe you mean "Model View Presenter" instead.

Jargon adds complexity to our writing that isn't needed. Each time a reader is presented with jargon or acronyms, they pause and think about it. This means their focus is shifted from the content to the words being used to convey the content. If I come across "MVP" in a document and lack enough context, those precious seconds are enough time for me to lose focus and forget the previous thing I read.

## Assumptions

You will always have to make assumptions about your readers as you can't possibly write an article for each type of user in the world. If you're writing an article about creating an API with Ruby on Rails, you can probably assume that your readers have some understanding of basic software development and the Rails framework. It's probably safe to assume that they have Rails on their machine. However, be transparent about these assumptions and provide links to pre-requisite documents to help users get started:

```
This guide assumes that you are familiar with Ruby on Rails and have it installed on your machine. If you're not familiar with Rails or don't have Rails installed, you may wish to check out [the official Rails documentation](http://guides.rubyonrails.org/getting_started.html) before continuing.
```

## Present Information as it's Needed

Introduce content as the reader needs it. If you're teaching me Java, I don't need to know the history of the language in order to get started with it. Likewise, readers don't need to wade through five paragraph introductions that cover subjects they won't get to for another 6 pages.

If our document outlines how to create an API using Laravel, we don't need to explain how APIs work in our introduction. A more appropriate time to explain API theory is as our readers are implementing it.

An outline of such a document might look like this (**Note:** An assumption was made that readers of this document are users who understand MVC or users who already use Laravel):

- Defining API and explaining our problem
- Installing Laravel
- Creating Models/Controllers to work with data
- Creating a DB schema and seed data
- Explaining that our "views" are JSON responses instead of HTML/intro to the API controller
- Making requests to the API
- [...]
- Summary of what was done/where readers can find more resources

I skipped a few steps in the middle, but you'll note that I introduced concepts as readers needed them. Instead of explaining that our API doesn't use views in the traditional sense, I introduced that subject as readers were preparing to use that information. This means the reader didn't have to file away that information for later and it reduces their need to scroll back to where the concept was introduced.

## Call Out Crucial Concepts

If the reader needs to know something in order to progress through the document, be sure to call attention to it. Bring it up each time they need to use the information.

If we're writing about API authentication, I'll make sure the reader is aware that credentials should never be sent in plain text. Every time we tweak our authentication layer, I'll mention something about SSL being in place. Before we talk about deploying an API, I'll make sure they include SSL as part of their deployment strategy.

## "Omit needless words." - taken from Elements of Style by E. B. White and William Strunk, Jr.

"My name is Amanda" versus "The name to which I am referred is Amanda." Remember that our readers are having a problem and we're telling them how to solve it. A document is an implied promise that you will help the user meet their goals, so don't waste their time on tangents. But, this doesn't mean your documentation has to be boring and dry -- if you want to write conversationally, do it.

## Don't Trap Users

In my `Introduce Your Solution` section, I walked you through tweaking a document title to maximize effectiveness. In the process, I negated the point I just made about omitting needless words. Now you're probably thinking, "Why would you show me this if it's not how I should do it?"

Exactly. Don't lead readers through a series of steps that result in failure in an attempt to "teach" them something. This will cause frustration and readers might even feel as if you're looking down on them.

The section could have been written like this:

```
Your title and your introductory paragraph work together to tell the reader two things: 1) the outcome of the article, 2) the problem this outcome solves.

Example: Your readers are trying to host websites on Ubuntu 14.04, and the solution is to set up a LAMP (Linux, Apache, MySQL, PHP) stack. The following title and introduction tell the reader the outcome of the article (a LAMP stack running on Ubuntu 14.04) and what problem it solves (allowing them to host a website). Together these things tell readers that this guide is likely to achieve their goal.
```

```
Title: Host Websites on Ubuntu 14.04 with LAMP (Linux, Apache, MySQL, PHP)

Setting up a LAMP stack will allow you to host websites on Ubuntu 14.04. [...]
```

```
The title isn't ideal as it contains an acronym that users may not be familiar with ("LAMP"), but it gives them enough information to decide if this guide is likely to help them. Even if they're not sure what "LAMP" means, the rest of the words tell them that this guide is likely to help them solve their problem. This title is also a bit long, but it explains the acronym for the reader while giving search engines some keywords. It also gives the readers detailed information about the problem to be solved and the tools used to achieve the solution.

The introductory paragraph explains what will be used to solve the problem and immediately reaffirms that the reader is in the right place if they are looking to host a website on Ubuntu 14.04.

**Note:** As a matter of preference, I will sacrifice Google ranks for usability every time -- I would rather add overhead to my day by linking the same doc 4 times an hour than have people organically land on a document that confuses them. I can usually find a happy medium.
```

## Careful Code Samples

Don't provide code samples unless you expect the reader to run them. For example, if you're trying to explain the repository design pattern to your audience, using an image to explain what's happening might go a lot further than showing the reader how to do it in a specific programming language. A code sample in the middle of an abstract concept shifts focus from the concept to the implementation details and may cause confusion. At the worst, readers are turned away because they don't know the language you've used in your examples. If you intend to use a specific language to convey an idea, make that apparent in your title:

- Using the Repository Pattern in Python
- Implementing the Repository Pattern in C#

### TEST TEST TEST

If you provide sample code it **must** work. Keep track of documents that have sample code and make an effort to test these samples regularly (ideally any time something changes).

### Comment EVERYTHING

Code samples without comments that explain them aren't useful to everyone. Code is only self-documenting if you're a subject matter expert and you can't assume that your readers will be. That's not to say you should comment every curly brace, but that one line statement that declares a variable? It needs a comment to tell the reader what this variable will be used for.

It's important that readers don't feel like morons for not knowing what a line of code does. Likewise, it's also important that readers don't feel like you think they're too stupid to understand basic programming concepts. Make sure your comments are useful to inexperienced readers and unobtrusive to experienced ones.

## Getting Help and Leaving Feedback

The clearest documentation will still be unclear to some readers. Sometimes your documentation is just plain wrong. Make it obvious that users can get help/report inaccuracies and direct them where to go to do so. Keep track of this feedback -- it's actionable and helps you develop stronger documentation!

## MAINTAIN

Your work isn't over just because you've released your docs. Once they're out there for people to find, you need to invest time in maintaining them. Make routine maintenance and testing part of your documentation strategy and allocate resources to it. Out of date documentation is a red flag -- if you can't be bothered to update it, what else are you slacking on?

## Grammar

I often ignore grammatical rules in order to make my writing seem conversational. Conversational writing might annoy your editor, but it'll make the subject less dry for your readers.

A basic understanding of language syntax (the written/spoken kind, not the programming kind) will help you create documentation that's mostly free of errors. In English, things like knowing the difference between their/there/they're and using apostrophes correctly goes a long way. Grammatical mistakes are noticeable and make you seem less credible, so have someone else look over your work for errors.

## Summarize

Summarize the problem and how you solved it. This is also a great time to link extra resources that might be useful.

In this post I have made the following points:

- Introduce the problem and its solution via your title and introduction
- Don't overdo jargon and acronyms in docs as they can cause confusion
- If you assume the reader is at a certain level before starting a guide, state so. Likewise for assumptions about tools they have installed on their machines.
- Introduce concepts as the reader is preparing to use the information to avoid overloading their brains.
- Call out and repeat important concepts and key takeaways.
- Don't take 50 words to convey an idea that could be explained in 10 words.
- Don't lead readers into a trap in order to teach them something. It's frustrating to spend time on something only to find out you've been set up to fail.
- Only use code samples if needed, and be sure to test them regularly. Code samples should be documented with comments.
- Tell readers how to get help or leave feedback if something isn't right.
- Include documentation maintenance into your documentation strategy.
- Be aware of grammar rules, but throw them out of the window if doing so helps clarify your documentation. (I'm notorious for ending sentences in prepositions.)
- Summarize what was done into key takeaways

That's all there is to it! If you have something to add to this, [send me a tweet](https://twitter.com/AmbassadorAwsum)!