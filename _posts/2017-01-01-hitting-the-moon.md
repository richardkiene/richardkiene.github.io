---
title: Hitting the Moon on the First Shot
---

I've been toying around with the idea of writing a post about the cultural
and mental shift I've undergone in the last year and a half at
[Joyent](https://www.joyent.com) for quite some time. The biggest transition
being going from "Ship ship ship, even if it is shit, ship ship!" to "Get it
right, preferably the first time".

In my opinion, the emphasis on upfront planning, architectural review,
academic-ish rigor, and fully understanding each problem set is what most people
coming out of a university with a Computer Science degree would like to be doing
to begin with. Unfortunately most people aren't lucky enough to fall into a
place like Joyent immediately and are subsequently subjected to cultures which
don't value these things at all. Consequently, incentives shift from what
brought a lot of people in to Computer Science (e.g. solving hard problems,
designing, making a difference, etc.) to simply getting the next feature out the
door without regard for longterm quality. The ship ship ship culture also breeds
people who work unnecessarily long hours and deal with a perpetual mess.

In my first year at Joyent, I had to battle a monkey on my back telling me
I wasn't doing a good job because I wasn't putting something in production every
day. I had to retrain myself to value getting it right the first time over ship
ship ship. The result is a better quality of life, better quality output, one
[feature](https://github.com/joyent/rfd/blob/master/rfd/0005/README.md) in
production for about a year without incident, and a monitoring and metrics
[architecture](https://github.com/joyent/rfd/blob/master/rfd/0027/README.md)
that is in early beta.

I have to admit, shaking the ship ship ship mentality was difficult. I
frequently found myself getting frustrated with conversations that felt like
a waste of time. These were conversations that previously would have been
deferred until the project was minimally complete. However, perhaps due to lots
of growing up, I realized that the culture at Joyent necessitated these hard
conversations about scale, future usage, debuggability, observability,
de-risking, and failure modes. So I kept an open mind (after all I took this job
in part to learn from the best and to grow) and embraced the culture.

What I found was that the conversations, rigor, design process, etc. all
resulted in solving problems during the design process that normally would have
been solved after realizing the shortcomings in production. The biggest
difference being that I, the engineer, pay the price up-front for my decisions,
rather than hoist them on to operations and support teams while I "figure the
rest out". To be clear, I'm not saying that I previously put no effort in to
designing and scaling my solutions. I'm saying that much of that effort
was done informally, often after the first cut was shipped. This was in large
part caused by the ship ship ship culture pressuring me to get my work out the
door as fast as possible.

At Joyent we have a process called "Requests for Discussion", or
[RFD](https://github.com/joyent/rfd) for short, that prevents such informal
design processes. The process is modeled after the
IETF [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) process, but
scoped to our product. Anything which might take a significant amount of
engineering effort (two weeks is generally considered the threshold) requires an
RFD to be written and some form of consensus within the team before any earnest
code based engineering takes place. Additionally, we use
[Gerrit](https://www.gerritcodereview.com/) to gate commits from going directly
to the shipping branch. Code must pass an automated `make check` and receive a
+1 for code review and integration approval from one or more members of the
engineering team before it can reach the shipping branch.

This might seem like a ton of red tape to prevent progress, but I assure you it
is not. Throughout my journey, I've continually been surprised by how many
problems have been solved upfront because of these processes. Many times I've
reached what I believed to be an impasse while writing my code, only to look
back at my RFD and realize I'd actually solved the problem and documented it.
These processes allow our team to help each other ship the best code we can, and
agree upon what we are going to do _before_ any code reaches production.

For me, one of the things that makes these processes work is that I'm not
dealing with a bunch of political infighting. It's not that we're without
politics and people with a competitive nature, it's that I'm able to trust that
my coworkers' critiques come from a genuine desire to make others better and to
produce the best product we can. This makes it far easier to take criticism via
code review or the RFD process when you know that the other person isn't simply
against _you_.

Furthermore, it is quite helpful that I'm working with a team of very
accomplished engineers. This aids me in checking my ego at the door. I don't
need to feel like I'm conceding ground by admitting I don't know something.
Instead, I can ask the dumb questions, learn, and improve myself and the
product.

Overall my quality of life, quality of work, and amount of learning has
increased substantially since joining Joyent. I feel like this is exactly the
kind of job I wanted to do after I earned my degree, but for whatever reason I
didn't find my way here until much later on.

There is a ton more to this topic, including mean time to failure vs mean time
to repair, arguments based on merit vs arguments based on politics, etc. Also,
this is not meant to refute CI/CD which are completely appropriate tools in
certain products and organizations. Perhaps in followup posts I'll address the
different production burdens that can necessitate or benefit from a different
shipping cadence, but the overall rigor that we exercise is still valuable
either way.

My hope is that this post will inspire others caught in the ship ship ship world
to challenge themselves and look for opportunities that let them be proud
of what they create.
