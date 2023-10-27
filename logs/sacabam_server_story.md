# ~~Quick~~ runup of servers I tried

A [*Sacabambaspis*](https://en.wikipedia.org/wiki/Sacabambaspis) story.

### How it started

[Click here to skip storytelling](#what-i-need)

<!-- [multimarkdown - How to link to part of the same document in Markdown? - Stack Overflow](https://stackoverflow.com/questions/2822089/how-to-link-to-part-of-the-same-document-in-markdown) -->

So after one year of procrastination, I finally made my first discord bot.

While the bot did not come from sheer personal interest, but rather an abomination of an unpaid intern during my bad times when I have to save my OPT, still. I'm not going to complain where my personal projects come from, as long as I actually started them. ~~(Which remains questionable up to this day.)~~

However, telling your CS illiterate boss that you're making bots for the project to launch, while leaving all of them open source, and also adding weird functions that are destined to not make profit, would make you way too suspicious, especially if you're also launching all of them on a 1,000USD/month AWS Server. ~~(which only cost that much because people are doing AI training in it, the bot itself costs maybe 5USD/month to run.)~~

Either way, all of this means that, after way too many years of avoiding servers because of the subscriptions they incur ~~(and how I tend to forget to check my bills)(speaking of which, I should probably start actually checking them)~~, I finally ended up having to look for a server, for my discord bots.

### What I need

A server (obviously), that...

- is stable (obviously)
- can hold a discord bot in Python 
  - (well, python for the time being. The only other language that's good at discord is JS, and I'm *NOT* going through `===`.)
- does not cost too much 
  - (even if I'm not broke AF (which I am), I'm not spending money on useless CPU power.)
- does not take too much brain to setup
  - time is limited, esp. when you also have to deal with your boss. 

I'll take "can't do too much things other than a simple running command" over "costing more / takes more brain to setup", as I genuinely don't need that much. I know myself well enough, that I'm 100% sure, if this takes any more effort than the bare minimum, I'll stop in the way of doing it.

### Sources

Most of these were found with a "How to host Discord bot" Google search. I'm pretty sure there are more hosting services out there, I was just too lazy on it. (which is probably good in terms of avoiding procrastination, and starting production of the actual bot.)

### Results

##### The ones that literally don't work: 

- bot-hosting.net
  - Free trial, gives you free server time if you watch ads, ultra cheap
  - *Extremely* unstable, disconnects after ~10 mins
    - not sure if this is a free server issue. not bothered to investigate, they didn't respond to my ticket either.
- Pylex
  - Free trial of 1 server, good price afterwards (2EUR/month)
  - Stable enough for a bot (esp. compared to bot-hosting, even though they use the same server panel FE)
  - panel super hard to login
  - only supports EUR for now (and great news, I'm in NA!)

##### The ones that actually (or probably will) work

- **Pebblehost**
  - 3USD/month, states that they take multiple bots in 1 server, provides code for you (not tested yet)
  - (hopefully) stable enough
  - I took this one in the end

-  Heroku
  - 7USD/month, might only be able to run 1 bot in it (because I'm bad at parallel)
  - probably has more control than Pebblehost, as it's the 1st one in the list to be an actual server, not just a hosting service
  - I'll probably switch to Heroku if Pebblehost somehow screws me up in the future (RIP wallet, in that case)
- Google Cloud/AWS
  - obviously would work
  - probably won't be that expensive
  - last resort for me, because I don't want to use my brain just for server hosting.
- Hopefully I won't have to update this in the future (10/27/2023)

### Conclusion

- I'm using Pebblehost for now
- Hopefully I don't have to switch in the future (or look for new ones)
- Probably not trying smaller platforms next time. Super cheap, but genuinely a hassle.
- I hope someone come help me solve CICD(?)
  - and I should be writing more stuff.

