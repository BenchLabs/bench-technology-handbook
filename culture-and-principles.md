# Culture and Principles

## What is culture?

What is culture? How do you point at a company and say: "this is their culture"? Can you look back at a period of time and understand how it influenced culture? If you don't like a culture, can you change it? How do you hire for "culture"?

Culture can feel ambiguous, intangible, and inaccesible. Fortunately, it isn't.

You can read, listen to, type, speak, and think the culture of an organization. It's right there, in the conversations that are taking place every single day. Every Slack message, every watercooler session, every Jira comment, every 1:1, every all-hands, every line of code; they are all conversations that we're having or have had. Culture is simply the sum of all of these conversations.

With this mental model, we have no choice but to accept that every single person who works here is actively creating our culture every single day, _every time they have a conversation_. No one is spared this responsibility! So what do we do with it?

## Culture creators

We've all been culture creators our entire lives, whether we knew it or not. Here's an example:

_You're at the pub with a group of friends, having a casual chat, when one of the people at the table 
participates in the conversation by saying something innapropriate. 
There is a pause, where everyone says to themselves: "do I say something?"
If nothing is said, the innapropriate conversation is deemed to be acceptable (at least by the perpetrator), and they may continue to act the way they've acted.
If something is said, the opposite occurs: a culture of standing up for a moral code is solidified, and the perpetrator will either need to change their ways, or find another table._

If we think of culture as the sum of all conversations, we can sketch this out as a formula:

```
If no one says anything:

All the conversations we've had + the innapropriate thing that was said = our culture

If someone says something:

All the conversations we've had + the innapropriate thing that was said + a conversation about how that comment isn't acceptable = our culture
```

It's that simple: one conversation changes the culture, and another may correct its course.

So, as culture creators, it is up to us to observe the conversations that we're part of. We must then ask ourselves: "are these conversations consistent with the culture I'm committed to creating?" If they aren't, it's up to us to make sure the our suubsequent conversations put us back on track.

## Culture at scale with principles

At the time this is written, Bench has over 500 employees distributed across North America. At this scale—in order to be able to ask "are these conversations consistent with the culture I'm committed to creating?"—we must explicitly define our culture. This is why we have cultural principles.

First, let's look at the Bench Principles:

- Keep it Human
- Be Responsible
- Get Scrappy
- Take a Stand
- Default Open

_We recommended taking a [deep dive](https://bench.co/go/culture/) if you aren't yet familiar with these principles._

These principles are designed to describe the _how we do it_ aspect of our culture. They intentionally read like instructions, and  are broad enough to apply to everything you do at work: writing an email, messaging a colleague, brainstorming with your team, commenting on a document, etc. They are designed to be in tension with each other. For example, _Be Responsible_ is often in direct tension with _Get Scrappy_, and _Keep it Human_ is often in tension with _Default Open_.

You can think of the five principles as the boundaries for conversations that are consistent with our culture. If a conversation exists within the boundaries of these principles, it is consistent with Bench's culture.

Next, let's look at the _[Technology Principles](technology-principles.md)_:

- Create Value
- Foster Growth
- Honour Time

Where the Bench principles are _how we do it_, the Technology principles are _what we do_. Like the Bench principles, they are designed to be in tension with each other. The ideal state looks like this:

>  We create immense value in the world while growing tremendously as individuals, and we do so on timelines that push us while also allowing us to live rich personal lives.

Sound idealistic? Of course it does. That's the point. This is the culture we're here to create, so why would we make it anything but incredible?

## Using the Bench and Technology principles together

As mentioned above, the Bench principles give instructions for _how we do it_, and the Technology principles give instructions for _what we do_. To use them together, it's helpful to picture them as a matrix.

![Image of principles matrix](images/principles-matrix.png)

So, when we have conversations about _Creating Value_, _Fostering Growth_, and _Honouring Time_, we must ensure that they live within the boundaries set by _Keep it Human_, _Be Responsible_, _Get Scrappy_, _Take a Stand_, and _Default Open_. If this all seems a bit complicated, don't worry: there's a system.

## A test suite for our culture

Each of the Technology Principles has a set of supporting principles. _Create Value_, _Foster Growth_, and _Honour Time_ are instructions, and their supporting principles are assertions. These assertions answer the question: "what needs to be true for a conversation to be consistent with this principle?" In practice, we've found that each assertion maps nicely to a Bench principle (though this isn't a hard requirement). This has a really interesting side effect: each assertion effectively becomes a unit test for a conversation.

For example, the supporting principle `We are most likely to do high-value work when we see it as necessary to advance a cause that we believe in` is a way to "test" whether a conversation is consistent with both _Create Value_ and _Take a Stand_. Similarly, `Successes and failures are important because of what we learn from them` is a way to "test" whether a conversation is consistent with both _Foster Growth_ and _Default Open_.

All together, the supporting principles act as a test suite for our culture. Every conversation we have, whether async or realtime, in a PR or in a Google Doc, can be run through the test suite to determine whether it is consistent with the culture we're creating.

Consider the following (made up but not uncommon) conversation: 

```
Manager: 
In our last meeting, you identified that you have a lack of expertise in what you're working on,
and we agreed that you would come up with some goals about how to get that expertise.
Can you share what you came up with?

Engineer: 
To be honest, I didn't have time to think about this because of my current deadline.

Manager: 
I totally get it. Let's come back to this when you're less busy.
```

If we run this through the test suite, we see multiple failures:

**Create Value**
```
Failure: The speed at which we learn is the most important factor in our ability to create value.
Reason: Prioritizing a deadline over growth limits the speed of learning.
```


**Foster Growth**
```
Failure: Growth happens when an individual accepts the monumental challenge of continuously asking themselves: is this the best I can do?
Reason: Using a deadline as an excuse for not focusing on their own growth.

Failure: To grow, we must step into conversations that feel scary and uncomfortable, and we must learn to differentiate them from conversations that feel unsafe.
Reason: Letting them off the hook for being busy instead of intervening in the excuse and standing for their growth.
```

**Honour Time**
```
Failure: Learning and doing are not separate endeavors. Within the time we allocate to a problem, we must account for both the need to deliver a solution and the need to properly learn _how_ to deliver it.
Reason: Somewhere in the planning process a deliverable was agreed on that didn't provide time for learning.
```

This tells us that this conversation is not consistent with our culture, and it also gives us a starting place for how to have the _next_ conversation to get back on track. In this case two things are happening: the engineer is letting a deadline take priority over their own growth, and the manager is letting it happen—despite having committed to the `Learning and doing...` and `The speed at which we learn..` supporting principles. That's not how we create value, foster growth, or honour time!

Guided by our principles, a subsequent conversation could be:

```
Manager: 
Last time we spoke I let you off the hook. You used a deadline as an excuse for not 
prioritizing your own growth, and I let you do it. Your growth is at least as important 
as that deadline! So today, we're going to figure out how to make time for it.

Engineer: 
To be honest it's just really hard to find time to think about myself.

Manager:
We find time for whatever we consider to be our top priority. Growth is a long-term investment 
and you need to keep making instalments! So, I'm asking you to raise the priority of your growth. 
This might result in a temporary slowdown in your project. To be clear: I'm okay with that.
Can you take this on, and give me your goals at our one-on-one next week?

Engineer:
You know what? I've been putting this off for too long. I'll give them to you by tomorrow 
so we can review them async before our meeting.
```

This time, the manager steps right into the uncomfortable situation, and doesn't let the engineer off the hook for de-prioritizing their own growth. Notice that this is done with respect and compassion—there is no blame placed, and it is phrased in a supportive manner. As a result the engineer gets fired up by suddenly seeing that they can make space for their own growth, and goes beyond the original request from their manager. _This_ conversation is consistent with our culture, and it sets up their next conversation as well.

In the event that a conversation doesn't fail any tests and _still_ feels inconsistent with our culture, we're probably just missing a supporting principle. If this happens, bring the conversation to your manager so you can run it through the test suite together and identify what's missing—as our culture matures, our test suite must mature with it.
