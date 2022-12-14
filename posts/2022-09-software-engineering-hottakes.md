---
author: "Arnav Gupta 💉💉💉"
handle: "@championswimmer"
source: "https://twitter.com/championswimmer/status/1548562274536763396"
---


A thread of some of the likely most unpopular and unconventional hot takes on software and programming.

All very personal opinions, most derived out of personal preferences, rather than logical/rational reasoning. 

I don't necessarily apply all these in practice though.

I don't think doing artificially created puzzles like LeetCode should be involved in early stage learning to code. 

Learning to build a website or app first, and coming to algo-gyms later in life is a better approach.

Or else people miss the forest for the trees.

People focus waaay more on "moving the logic from O(N) to O(log n)" for optimisation, when in the real world "each iteration touching the UI thread vs batching UI updates" type of things actually make a dent on performance.

Also vs LeetCode, one more heavily underrated resource is HackAttic

As a good developer you should be able to solve all the challenges on it. In reality, 90% junior devs, and 50% mid level devs would struggle with a bunch of them

Those challenges are literally ur bread &amp; butter

I wouldn't take hiring/appraisal calls based on it, but on a personal level I totally judge developers on having shell and CLI chops. 

GUI and mouse bois can surely be good devs too, but the productivity unlock on being nifty with shell is whole different level.

To understand the scope of productivity unlock imagine requiring the bandwidth of a dedicated video editing person and involving man-hours of work, file transfer etc  vs someone who can ffmpeg their way into splicing some videos, transcoding them and getting shit done in seconds

Another thing (again I work hard to keep workplace biases in check regarding this) but I have absolutely never ever seen a good dev *NOT* being absolutely pedantic about comments and commit messages. Again &lt;1% people are like this, but it correlates absolutely always.

You might wonder if the greats, the ninja programmers, the 10x engineers, who move mountains, give a shit if whitespaces go around braces or inside them. 

And yet, the sharpest folks I know set up a linter in their project before writing their first meaningful line of code.

I'll come to some very opinionated and very personal preferences and inclinations in terms of tech stacks and languages. 

I'll go with hottest of all takes. Go is an absolutely abused, mis-intended and dumpster fire language, for of the use cases it is used today.

I want a tiny binary, for a monitoring/logging agent, or a systems tool like docker agent, or kubectl, fantastic, Go (or Rust) is the best language to go for. 

I want to make REST APIs, and some DB calls - no worse choices than Go to do that. Even Python and Node are far better

99% of the "concurrency" benefits Go touts is just offloading IO and network into goroutines (which you have to largely manually manage safe concurrency for) - is available out of the box in something like NodeJS via internal I/O APIs, without manually managing safety

Not unsurprisingly, the stack with which beginners create high concurrency web servers best is NodeJS, vs other stacks where beginners either cannot easily achieve concurrency (Python, Rails) or screw up context and memory leaks (Java, Go)

Okay, databases. 

MongoDB is a veritable cancer on the face of this earth. Not because it is always bad, there are some places it *might* be good, but my god, the level of marketing and evangelism, has made it the biggest bane of the software world.

99% of info-system software should be just Postgres (and Redis). 

Maybe 99.99% is a better estimate. 

Except the analytics data and stuff, for which Clickhouse type things are required.

About languages, another thing - learn Java. 

I don't use actual Java a lot now a days (Kotlin for both Android and backend), but one thing, in your devleoper career one can never run from is understanding the JVM.

Between Java, Scala, Kotlin and search tools like ElasticSearch and Solr, or for old school data houses using Hadoop, I don't think there are *any* tech companies in the world that do not use Java or something JVM based

The career penalty for not knowing Java is incredibly high

On that note, Java is actually a fairly good language. 

A Spring app, packed into a GraalVM image, gives you all the single-binary-ness Go touts, with a way more mature ecosystem (a library for literally everything, all answers on SO), and significantly better dev experience.

Oh, and talking of developer experience, I've totally come to judge folks who do not invest in good IDEs and put effort into setting up their (digital) workspace. 

Like, oh man, what productivity 10x you get from Jetbrains IDEs and some of the popular plugins.

Seeing someone with all their keyboard shortcuts setup, doing things like "test this line of code" and debugging with a proper breakpoint debugger, and using all the refactoring features is just 🤌 ASMR

I'll add some frontend hot takes too. Starting off with the most controversial 

I feel both Angular and Vue to be better than React. Vue has been going downward and losing the plot since 3.0 though

MVVMs are great for frontend. Pure immutable state functions that emit UI is 👎

It is a mathematician's intellectual maturbation that everything can be output of a function and pure state functions run the world. 

Web UIs are not that. They are too interactive, and forcefitting a statemachine to the smallest button press creates very convoluted state mgmt

This one's a personal opinion. I love template based UI design waaaaay over composable things. HTML, XML, mustache syntax for injections, are great. 

I don't get the craze for JSX, Flutter, Compose style way of UI building. 

This, I get, is how my mind looks at UI. Ymmv.

Going to add some more here. Next up: services

"services" are great. Microservices, serverless, kubernetes type orchestration, auto scale up/down etc are terms I vigilantly run away from

Nginx + node monolith + cloudflare caching GET reqs = easily 1M user throughput on $50/mo

Something like user/auth, analytics, and straight up pure in-out workloads like eg image uploads, NLP workflow to tag data, payments processing, email/SMS sending can for sure be developed as a separately spun up server. 

Mostly these do not impact UX latency directly too.

But I still cannot believe how many times I have been consulting on some very early stage startup, hitting "perf" issues on slight scale, and digging down, it always is actually because of the overhead of API gateway, service discovery, queue and worker spin up times etc

Not so well known fact: Read replicas of DB with larger thread pools + simple horizontal scaling with the most basic nginx based loadbalancing usually gives 100~1000x speedup without even optimising DB queries or anything high effort "optimisation".

Microservices and distributed computing just makes things unnecessarily hard. 

Some engineers love playing the game in hard mode. But in most companies you have limited respawns available. There are no points of playing hard mode and dying before killing the boss

Remembered another thing regarding comments. 

I highly correlate quality engineers mentally with large trails of // TODO: comments left behind. 

Every commit is unfinished. Some people just document that shit, some don't.  

Again personal bias, but mostly checks out.

Why no continue the violence into Monday too. Let me add some more here - re: API design. 

GraphQL is in the same bucket as MongoDB for me. Absolute dumpster fire, over-marketed, over-hyped, and used in 99.99% cases where CRUD-over-REST should have been.

Again, *maybe* some cases where GraphQL is better. (Don't come at me with - "Github API is graphQL", it is the only corner case in the world full of 100s of open APIs in the world)

Largely though, young teams are giving up default caching of GET reqs, and doing in-memory joins

To you frontend folks - just bloody learn talking to CRUD endpoints. Your relationship to the backend is similar to backend's relation to the DB. You have to put in the work

There can't be this magical "single firehose of data that answers whatever I ask"

99% startups using GraphQL will see a 100-1000x perf gain (and might not need horizontal scaling on the API server) if they used REST instead of GraphQL. 

So much compute wasted by in-memory joins of those silly Apollo-based controllers. Also 99% GET reqs will be 304 now

