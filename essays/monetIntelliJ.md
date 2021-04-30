---
layout: essay
type: essay
title: If Claude Monet Used IntelliJ
# All dates must be YYYY-MM-DD format!
date: 2021-04-29
labels:
  - Design Patterns
  - Pblication-subscription Pattern
  - Observer Data Pattern
  - Advice
---

The artist Claude Monet, creator of various masterpieces, painted pieces of art out of a single element: a dot. Monet was famous for creating 'impressionism' art, a way of painting in a local, seemingly isolated spot of a canvas and working away and around that spot. The interesting thing about an impressionist painting is that it does not look like much up close, besides a bunch of splotches and scratches. However, when you take a couple steps back you realise the grandeur, foresight, and skill needed to transform unassuming dots of paint into a masterpiece. I do not believe that it is unreasonable to notice the distinct and even abstract design patterns employed both in boundless impressionism and the technical practices of software engineering. Writing software is, in its own regard, much like impressionism. Read more to find out why.

When I first encountered writing JavaScript code in the Meteor application environment, I was extremely overwhelmed by the numerous directories, funny-looking functions, and foreign keywords. I spent hours upon hours trying to dissect pieces of sample code provided by my professor, trying to understand how everything in the seemingly endless dropdown of directories could possibly make any sense. What I did not realize then was that I was looking too close at code without understanding what the code was trying to do, or in impressionist terms, I was looking too closely at the dots without understanding or appreciating the big picture.

To address this, I learned a thing gor two about common design patterns. Design patterns in software engineering facilitate the visualization of how a project will link seemingly chaotic and esoterically written pieces of code into a sophisticated, well oiled project. To put it plainly, design patterns are 'molds' or layouts of ways to organize code. These layouts have proved tried and true and although they are various, they are consistently found across nearly all pieces of software. These patterns are the ways that software engineers construct and organize their code to offer similar functionality, readability, and modularity while still retaining the freedom to construct various distinct and independent projects.

Keep in mind, these patterns are just that: patterns. They are the consistent practices that the majority of software engineers employ to organize their code, they are by no means necessary. There are even outdated and 'bad' design patterns. However, by conforming to documented and established patterns, you are able to express your ideas freely to other software engineers and achieve modularity and readability across disciplines. This should theoretically increase efficiency and decrease confusion.

By now, I hope you understand that I like to make sense of things via metaphor, analogy, and allegory. The code fragments that I was once intimidated and confused by can be thought of as dots in one of Monet's paintings, seemingly meaningless alone but beautifully harmonious once you understand the big picture or in this context, the design pattern that it is part of. The dots in Monet's paintings do not individually make sense, their value is purely in its relation to others and what it adds to the final product. In this case, code fragments alone do not make an application, nor do singular design patterns alone make an application work. It is the way that various design patterns mingle and interact with the individual code fragments that create the working application. And then, and only then, can an application function AND be appreciated and understood by your fellow software engineering peers.

While in no way do I claim to be an expert in either impressionism or software design patterns, I however have run into a fair share while working on a group project in my software engineering class. Below I will continue to discuss two design patters, the publication-subscription pattern and the observer's reactive data design pattern. Both are some of the design patterns that my team and I have included and I will explain how they relate to the broader practices used by other software engineers.

## Publish-Subscribe Design Pattern

Perhaps one of the most notable feature of a Meteor application is the way that data is passed around and accessed from the database, i.e the publication and subscription model. This pattern was one that confused the heck out of me. Before trying to even understand what was going on I focused on syntax, keys, and mysterious functions, I was looking too closely at the picture. Taking a step or two back helped me to understand the big picture and helped me to realize that the publication-subscriptions model is an amazingly beautiful process. Pictured below is a 'Users' collection that stores data for a user of the application, BowedIn.

```
class UsersCollection {
  constructor() {
    this.name = 'UsersCollection';
    this.collection = new Mongo.Collection(this.name);
    ...
```

Now what do we do with this data? Publish it to users of course!

```
Meteor.publish(users.userPublicationName, function () {
  if (this.userId) {
    const username = Meteor.users.findOne(this.userId).username;
    return users.collection.find({ owner: username });
  }
  return this.ready();
});
```

And finally, consider what happens if users need to access their data to edit it. We set up 'Subscriptions' within individual JSX pages and components that have the ability to access the database by virtue of the publication (pictured above).

```
const subscription = Meteor.subscribe(users.userPublicationName);
```

It is important to note that we certainly did not invent the publication-subscription model. This pattern is present in almost every full stack Meteor with React application. If you are new to the Meteor application structure and React components, it is totally understandable to feel lost and overwhelmed. Chances are that you haven't seen the syntax and keywords mentioned in the images above. My advice would be to look at what the code like you would a painting, appreciate the overall piece first before analyzing the dots.

## Reactive Data

The second idea I would like to discuss is the idea of reactive data. In my software engineering class we use JSX along with SemanticUI with React. The technicalities of how this exactly works is not necessarily complicated, but deals with an idea that is probably unfamiliar to budding software engineers. Reactive data creates an almost 'automated' feel to the code in the sense that you will typically have one class within a JSX file and a event handler function: onSubmit or onClick that calls a method within that class to handle the change in state of data. Below is the beginning portion of a render method in the BowedIn code. You'll notice that there is a nested <Redirect > element at the beginning of the class. This did not make much sense to me when I first started out with Meteor, I thought that a page is rendered at most one time and therefore it would not make sense to redirect to a different page right off of the bat. However, as you will see, the Redirect is for the time that the page is re-rendered. Take a look:

```
render() {
    const { from } = this.props.location.state || { from: { pathname: this.state.redirectTo } };
    if (this.state.redirectTo) {
      return <Redirect to={ from }/>;
    }
    ...
```

What actually causes the re-rendering of a page is when the user presses the 'submit' button. Notice at the end of this Form component (pictured below) there is a line:

```
<Form.Button id="signup-form-submit" content="Submit"/>
```

This lets Meteor know to call the 'submit' method:

```
submit = () => {
       const { email, password, choice } = this.state;
       Accounts.createUser({ email, username: email, password, choice }, (err) => {
         if (err) {
           this.setState({ error: err.reason });
         } else {
           // student redirect
           if (choice === 'student') {
             this.setState({ error: '', redirectTo: '/studentsignup' });
           }
           this.setState({ error: '', redirectTo: '/companysignup' });
         }
       });
     }
```

The interesting thing is that after the Meteor application executes the contents of the submit method, the render() method will be re-executed. This is where the conditional if statement gets evaluated and the Redirect happens. The Redirect will happen by virtue of a state change you might have noticed within the submit method (pictured above). When the submit method is called, the database and internal state will be updated, Meteor will detect a change in state and this will cause Meteor to re render the page and perform Redirect.

I have only discussed a few design patterns, keep in mind that there are many out there. I implore you to use an understanding of design patterns to understand how pieces of code contextually fit in and what they contribute to the overall application. For new developers starting off: try to keep in mind that applications are often constructed like impressionist paintings, they don't necessarily make sense when you look to close for too long. Try to take a step back understand the bigger picture first. Understanding some common data patterns is an excellent way to start.
