---
layout: essay
type: essay
title: Good Intentions, Bad Questions
# All dates must be YYYY-MM-DD format!
date: 2021-01-28
labels:
  - Question asking
  - Learning
  - Advice
---

The point of a question is to receive an answer, right? Notice the irony as I ask a rhetorical question. I’ve sent previous professors and teaching assistants long winded questions, completely over exhausting their patience and tolerance. I would then wonder why they responded vaguely and enigmatically. This led me to wonder if there was a way to engineer questions to get a desired result. “Perhaps I should not be unhappy with the answer I received, but try to fix my question”. As an example: “Do you believe in aliens?” is contextually different from asking “Do you believe intelligent life exists somewhere in the universe?”, the difference is subtle yet one person might not give the same response to both questions. The first question might assume if you believe in malignant humanoid Martians, and the second question seems scientifically plausible. This notion of questions having pre-standing assumptions, as you can imagine, extends beyond this example. Let’s transition from aliens to the world of intricate software engineering and find out how we can formulate questions to get desired results.

Software engineering is full of technicalities and it is important for one to understand context and jargon and more importantly how to apply it to one's advantage. This is where asking smart questions comes into view. It is unlikely that one will progress through one’s career without the assistance of another. In such an event, one might consider asking a question hoping to get a response in a timely manner, if at all.

Fortunately for us question-askers, there is a guide published by Eric Steven Raymond called [How To Ask Questions The Smart Way](http://www.catb.org/esr/faqs/smart-questions.html). It is an article that details some common pitfalls many might fall into when asking questions that will not warrant desired responses. A good way to summarize his article is the notion that like begets like, an answer is only as good as its question. If you write an essay long question about why your code does not work on an arbitrary line, you probably won’t get a response. If you just post your code and expect somebody to work through it, nobody will. Let’s take a look at some examples I found on StackOverflow and I’ll explain some points that Raymond makes.

## Here's a Good Question

First, here is an example of an EXCELLENT [question](https://stackoverflow.com/questions/65536137/convert-all-number-abbreviations-to-numeric-values-in-a-text-file) . This user’s heading is succinct and to the point, It entails everything that they would like to be answered and nothing more. There is no ‘fluff’ or unnecessary wording that might detract from the point of the question: how to “convert all number abbreviations to numeric values in a text file”. This illustrates a point that Raymond makes “Volume is not precision”. 

The user further explains their own attempts! This part is crucial, in context of asking the question, they have gone the extra mile and provided some substance to the question. They are not asking someone to solve the problem for them. Rather, it becomes clear what the user wants answered and what the user will receive in return and it becomes that much easier for someone to answer and correct the specific error. 

The responses to this question demonstrate the fruitfulness of asking smart questions. This question received nine responses that all address the very specific concern in a very specific way. Problem solved!

## Here's a Bad Question

Now, let’s look at a bad example. An easy way to spot some bad questions is to look at the section of StackOverflow: unanswered [questions](https://stackoverflow.com/unanswered). This thread is littered with millions of bad questions. For brevity, let’s look at [one](https://stackoverflow.com/questions/49162455/how-to-use-classes-to-control-dreams). While this question might look harmless on the surface: “How to use classes to ‘control dreams’?”. This with some context would not be a problem. ‘Some’ is the operative word. Gleaning from the question above, “volume is not precision”, this user included too much information! More information and background than this essay perhaps! First off, the user includes three GitHub links with the expectation that the reader will take the time to analyze all three articles.

This user then includes 50+ lines of code with absolutely no context and undefined methods, variables, and classes. After all of that, the user includes “Could someone please guide ME in the right direction here? I would greatly appreciate it.”. (The audacity, I know).

The real downfall of this question is that there is no clarity within the actual description and this causes the reader to become lost and fatigued while reading the question. I tried to read through the question and by the end of it, I could not identify what the user was asking. Mainly because the question is not explicitly defined!

I do think that this user would benefit from scaling down this question. Instead of submitting his 50 line excerpt without context, he should probably ask questions pertaining to individual methods or classes then work from the bottom up. Instead, this user throws some articles and code at the reader and expects the reader to find the problem (thereby inadvertently figuring out what the original question was!). It is no wonder that this question has been viewed thousands of times without a single answer.

## What did I learn?

In conclusion this has taught me, and hopefully you, a lot about asking questions - but nothing groundbreakingly new. I also learned that some questions may have hopeful intentions but ruin themselves. In the case of the bad question, the user put much effort into the question and was probably hopeful to get a response. But because they were not actually asking a specific question, they might never get a response. As someone who gets lost in the big picture when developing code, I know that in the future I will be certain to narrow down my concern, be as precise as possible, and ask directed questions with appropriate context. With this, I am hopeful. 

Happy Coding!
