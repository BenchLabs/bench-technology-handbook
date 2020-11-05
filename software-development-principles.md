# Software Development Principles

This document seeks to encode the principles that guide and direct Bench’s engineers in developing good software. 

What is good software? Good software:
- reliably performs the functions it was designed to do - this is #1, nothing else matters if this is untrue
- is easily usable by the end users
- is resilient, it can withstand errors and unexpected circumstances
- is understandable and maintainable by software developers, even those that didn’t write it
- is testable, meaning any bit of code can be automatically tested and said to be “correct”
- is observable and measurable, that is, it is possible to see what it is doing, and how well, at any point in time

The ideal of the principles laid out here is that following them results in us achieving the points above.


---

## Keep change small and to the point

There are many reasons to limit the amount of code that is changed or added at once:
- allows the author to focus on ensuring the changes are good and correct
- it puts less burden on code reviewers. Large PRs tend to get less thoroughly reviewed and it is indeed harder to spot problems
- any bugs or unwanted behaviours that result from the code going live are easier to track down and reason about
- if code needs to be rolled back, we can go back a single step instead of many 

In fact, this principle contributes to _all_ of the good software points above.

To follow this principle, pull requests should strive to address a single effect, whether that be a bug fix, library upgrade, a small refactor, a small feature,
or a small logical component of a larger feature.

Note: This is _not_ to preclude the possibility of improving the quality of the code around your change as you go, but even those must be in a close relationship
with the actual changes. If it starts to spin away, it's time for a separate ticket and PR.


---

## Quality over speed, but it's close

There is always a tension between shipping code of perfect quality and shipping code as fast as possible (by quality we are referring to the code itself and to
the software product). One can choose either option to the expense of the other but, as with anything done to an extreme, it leads to bad outcomes.

Focusing only on quality will cause software to ship unacceptably slowly, and ends up not being worth the time invested. Conversely focusing purely on shipping as fast
as possible leads to poor code, bugs, and bad user experience. It also ends up significantly slowing down the development process down the road as the team
struggles to keep up with bugs as well as the increased burden of working with difficult code. Simply put, it produces too much tech debt.

So where is the balance? Because too much speed has such a detrimental effect on the development of good software, we should favour quality. Code of consistent
code quality will allow us to maintain a more predictable and constant velocity, as we focus adding features or improving the system instead of chasing tech
debt. But, we always want to keep in mind that our job is to constantly produce value via software, so once our code is of acceptable quality, its time to _ship
it_!  

To put this principle into practice in a shape-up world, remember that although timelines are not variable, scope is. If something cannot be shipped of
acceptable quality by the end of a cycle, the scope must change.
