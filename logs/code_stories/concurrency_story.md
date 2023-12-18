# Ways to achieve concurrency ~~that I know about.~~

another title: So I was supposed to polish my resume...

### Okay, so why does it matter?

You usually won't come across architecture problems until you...

- take a course, such as Distributed Systems & Cloud Computing
- enter one of those big tech company
- encounter someone who know about this stuff (school/work)
- ~~are forced to polish your resume, and you have to add something that makes you look good~~

But apparently it's one of the more "advanced" topics, in that

- you train for certain toolsets just to use it
- it's crucial to any larger system
- it's (probably) a proof that you can write industry-level software (industry level in user scale)

TLDR, you get to skip it at school, but there's no running away from it if you're doing anything that's not front-end / Machine Learning.

### So what is it?

From what I currently see, parallelism/concurrency/high throughput systems/distributed systems all focus on one thing: **splitting the load between multiple clients, so that they don't have to be good(and expensive)**.

This could be:

- delegating part of the operations to another service 
  - such as using AWS EC2 - API gateway - lambda, and encapsulating stuff into a REST API
  - This is obviously *not* considered as high concurrency/a scalable system, but it *is* a distributed system - according to GPT, at least. (Well, you did distribute the workload between multiple stuff, so...okay?)
  - Usually the connections are more simple (compared to the next one) - REST APIs, Database CRUDs, web hooks and events...at least you don't need a message queue.
- assigning multiple instances in the same service
  - Which is extremely complicated, due to the amount of management involved - more on that in the next section (probably).
  - But also extremely useful, as it increase system robustness and throughput, while maintaining an acceptable hardware cost
  - And apparently is everywhere in big tech.

An easier imagination scenario would be:

- Pull out a toy project, and give it 1,000 users consecutively
- imagine the throughput size, and speculate what it would cost to handle that throughput
- and (probably) make a distributed system out of it ~~because that's what attracts HRs in resumes~~

I'll mostly talk about the second one (distributed system in terms of throughput) in the rest of the story, because anyone that's heard of front-end/back-end probably has *some* knowledge on how the first one (distributed in terms of layers/processing scopes) can be made.

### So how would you do it?

So from what I heard (as of 12/16/2023), a parallel system that allows high throughput, would involve the obvious...

- multiple servers
- one of them being a "main" server that controls every other one
- and a bunch of "workers" that does the heavy-lifting.
- message queues, to
  - allocate work to each worker, and 
  - keep track of worker load
- load balancing algorithms
- and "anti-crash" algorithms, such as
  - re-distributing the workload of a dead worker
  - allowing another server to take charge when the main server is down.

And of course you don't always do that from scratch, but even just learning pre-existing libraries is a big task on its own.

stuff that I heard include:

- Python series: Flask - Celery - RabbitMQ - mongo (not including failover and other robustness stuff)
- Java series: Spring boot (with included parallel stuff) - Hibernate - MySQL (maybe, or you can use mongo, doesn't matter that much)

Which I probably won't touch soon ~~mostly because upscaling a preexisting server is usually way more stable on toy projects~~.

---

### Changelog:

12/16/2023: I wrote this only to clear out one of my scrap paper that had notes about "tech stacks that seem really powerful". Oh well.