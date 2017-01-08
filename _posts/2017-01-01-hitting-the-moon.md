---
title: Hitting the Moon on the First Shot (or Valuing Correctness)
---

I've been toying around with the idea of writing a post about the cultural
and mental shift I've undergone in the last year and a half at
[Joyent](https://www.joyent.com). The biggest transition being going from
"Ship ship ship, even if it is shit, ship ship!" to "Get it right,
preferably the first time".

In my opinion, the emphasis on upfront planning, architecture review,
academic-ish rigor, and fully understanding each problem set is what most people
coming out of a University with a Computer Science degree would like to be doing
to begin with. Unfortunately most people aren't lucky enough to fall into a
place like Joyent immediately and are subsequently subjected to cultures which
don't value these things at all. Consequently, incentives shift from what
brought a lot of people in to Computer Science (e.g. solving hard problems,
designing, making a difference, etc.) to simply getting the next feature out the
door without regard for longterm quality. The ship ship ship culture also breeds
people who work unnecessarily long hours and dealing with a perpetual mess.

In my first year at Joyent, I've had to battle the monkey on my back telling me
I'm not doing a good job because I'm not putting something in production every
day. I've had to retrain myself to value getting it right the first time over
ship ship ship. The result is a better quality of life, better quality output,
one [feature](https://github.com/joyent/rfd/blob/master/rfd/0005/README.md) in
production for about a year without incident, and a monitoring and metrics
[architecture](https://github.com/joyent/rfd/blob/master/rfd/0027/README.md)
that is in early beta.

There is a ton more to this topic, including mean time to failure vs mean time
to repair, arguments based on merit vs arguments based on politics, etc. Also
this is not meant to refute CI/CD which are completely appropriate tools in
certain products and organizations. Perhaps in followup posts I'll address the
different production burdens that can necessitate or benefit from a different
shipping cadence, but the overall rigor that we exercise is still valuable
either way.

Overall my quality of life, quality of work, and amount of learning has
increased substantially since joining Joyent. I feel like this is exactly the
kind of job I wanted to do after I earned my degree, but for whatever reason I
didn't find my way here until much later on. Hopefully this post will inspire
others to challenge themselves and look for opportunities that let them be proud
of what they create.
