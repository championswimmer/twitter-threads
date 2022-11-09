---
author: "Arnav Gupta 💉💉💉"
handle: "@championswimmer"
source: "https://twitter.com/championswimmer/status/1533906614738391040"
---

Often when people discuss "100 unicorns in India" and "2nd largest tech startup hub" etc, the same people often are also talking of how "India hasn't produced a Facebook/Google". 

There's a reason to it. There are extremely few *actual* tech-first companies in India.


Yeah, your tech headcount might be the largest, or your SDEs might be paid 90 percentile in the market, or you make have a rockstar exFAANG CTO. None of it necessarily make you truly a "tech first" company though. 

How many unicorn sized Indian companies have a tech blog?


How many unicorn sized Indian companies have published open source tools that are actually widely used across the industry? The answer is abysmally close to 0. 

Take the example of StatsD 

[github.com/statsd/statsd](https://github.com/statsd/statsd)


This is a metrics collection demon, you can sort of use if you cannot afford DataDog. (These days you do have Signoz and all). 

I remember back in 2017, I was considering this for my startup. And I was surprised to see it was made by Etsy, which I discovered is a craft store


Like I couldn't imagine that a D2C-tech or a jwellery store in India would just even have the DNA (forget the intent, and then the investment) to build an infra monitoring daemon, and good enough to open source, and become pretty popular in the industry.


If you take away [@getpostman](https://twitter.com/getpostman) or [@HasuraHQ](https://twitter.com/HasuraHQ) who, well, are developer tools themselves, how many of the Indian scaleups that are actually considered "good tech companies to work at", even, making tools good enough for the rest of the industry to use?


And no, I'm not saying "make something open source" should be a business level OKR (that's ridiculous) or even a goal. You are building a product, selling it, running a business. You're not in the business of making developer tools.

But when you move beyond writing the same old CRUD APIs to move data from point A to B, you're sure to find technical challenges which you'll solve for the first time

And if you're truly "tech first", you'll build a solution you'll feel proud to stand behind and show the world


If you're not building that. If you're just doing the bare minimum to make shit work today, and not actually building something that'll stand the test of time, ofcourse you'll not have much to show.

A lot of people in the startup circles seem to think that "we are equally good", (misguided patriotism or just delusional), I've heard say things like, what's the big deal about Uber or Amazon, even we have built Ola and Flipkart. 

Geez, will, you just please?


I mean, Uber is working on a whole different plane, where, to make iOS and Android teams work in tandem, they made their very own cross platform mobile framework (RIB) which is now used by many other teams. 

They made a tool to run a different build system for faster app builds.


Amazon made cloud infra on which half the world's banks and governments are running. 

Netflix has created half the ecosystem on which Spring Boot microservices work now a days.


Ok, so what's the difference, what's the secret sauce? 

I don't think I have a complete answer to it, but I have my experiences from which I can make some guesses. 

I'll take the example of what I saw when I moved from Zomato to Target.




Now Zomato, in the Indian ecosystem, is fairly an established tech player (heck, first of new age tech cos to IPO), and is considered to be a good place for engineers to go and work at. Pays fairly well. 2M+ orders, 5M-ish DAU, fairly high scale I'd say.

Now Target, scale wise, was actually slightly behind Zomato when I moved (DAUs and daily orders), but waaaay in revenue ofcourse ($ vs ₹). Doesn't pay top of market, and isn't like among "top 10 tech places to go work" by far. Not at all in the US. Tech = IT there.

Target doesn't have a CTO, it has a CIO (chief information officer). You get what sort of company that is. 

Nevertheless, having actual EMs, and "real" seniors (here in Indian startups 4 YoE folks are called seniors, what a sham), makes such a big difference.

And the other difference is how engineers actually work. It isn't about pushing a ton of code. 

Major architectural changes need to go through an RFC. 

New features, modules need to be accompanied by architecture docs and system diagrams


i.e. you actually have to think before you code. 

And what allows this to happen? Existence of competent EMs. 

Here in Indian tech companies, vast majority of tech teams are micromanaged by PMs. 

There are even SDE -&gt; PM reporting structure at places.

A junior SDE reporting to a senior PM, reporting to a business unit head. Recipe for creating bad tech, all the time

On frontends, it is not uncommon for designs being made, PRDs being drafted, and code actually being written, all parallelly

At 10M+ user, post PMF places. Sigh

