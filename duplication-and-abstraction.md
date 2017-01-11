Duplication and Abstractions
===

Originally talked about by Andy Hunt and Dave Thomas in The Pragmatic Programmer. (Need to read exactly what they said about).

A lot of developers know that they shouldn't duplicate code.  It makes logical sense.  You don't want to have to maintain the same code in multiple places because if it needs to change you have to hunt through the code base trying to find it, you'll likely have to write multiple tests to cover the same piece of logic, and you may find the duplicated logic starts to deviate over time leading to different behaviours which may be bugs.

However I believe that developers (I suppose I'm really talking about my past me here!) can focus on removing duplication by any means necessary, which, whilst solving the problem of the code being in more than one place, doesn't always produce a pleasing design full on reasuable abstractions.

*TODO: I need to read to rest of Don't Repeat Yourself and Othogonality sections of The Pragmatic Programmer again to make sure I'm right about this, but...*

In fact, Andy Hunt and Dave Thomas who introducted the concept in [The Pragmatic Programmer][], which is an excellent book and I encourage those who haven't read it to do so, spend a long time explaining different types of duplication and the ways they can arrise, but they don't offer any advice on how you should get rid of the duplication.

What I want to draw attention to is the link between abstractions and duplication that Steve Smith talk's about.  Steve Smith, in his entry to the book [97 Things Every Programmer Should Know][], says:

> The developer who learns to recognize duplication, and understands how to eliminate it through appropriate practice and proper abstraction, can produce much cleaner code than one who continuously infects the application with unnecessary repetition.

Removing abstraction through approriate parctice and proper abstraction.  It's this link between duplication and abstraction which I think holds the key to improving our designs.  One way our designs can improve is by replacing duplication with appropriate abstractions.

The hardest thing about this advice is there is no process you can follow to create the perfect abstraction, it really is were the art and creativity come in to computer programming and design.  The best guidance we have available are hueristics that describe what a good abstraction might look like, and others that indicate where we might be missing an abstraction.  Repeated code is an example of the latter.  It is a signal that we might be missing an abstraction.  If we find an abstraction that enables us to remove the duplication, we can replace the duplication with that abstraction.  However, if we naively remove the duplication, we may couple concepts together and reduce the reusability of our code.

To do
---

* Look for an example of bad duplication removal.  Perhaps I could use the QuestionGroups/Questions, or the API Services base class, or the API Modules base classes.  I could also try and find the proxy step where I originally started to think about abstractions.
* Look at DDD duplication between bounded contexts.
* Bring in what jbrains talks about in his video [A Long Look Down the Road (paywall)][] in his World's Best Intro to TDD course 
* There was an interesting stackoverflow post that I read sometime on stackoverflow about duplication.  I wonder if I could find that again.
* It looks as though Code Complete might have something to say on the matter.  I've never read it, and we've got a copy!
* Perhaps I need to research what an abstraction is.

[A Long Look Down the Road (paywall)]: http://online-training.jbrains.ca/courses/wbitdd-01/lectures/140743 "A Long Look Down the Road (paywall)"
[97 Things Every Programmer Should Know]: http://programmer.97things.oreilly.com/wiki/index.php/Contributions_Appearing_in_the_Book "97 Things Every Programmer Should Know"