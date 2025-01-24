+++
author = "Jonathan L Meek"
title = "Setting Up Meek Notes"
date = "2025-01-24"
description = "The definitive why and what tools used for meeknot.es"
toc = false
tags = [
    "meta",
    "blog",
    "hugo",
    "sourcehut",
    "hover"
]
+++
## Origin Story of MeekNotes
I have always wanted my own corner of the internet but never sat down to take the time to do this. Since 2020, I have debated with myself about creating my own blog. In 2024, I paid the money for this domain name and got to work. Most of the time the site just sat there with me debating about which service to use, what static blog generator and what theme with the static blog generator. I am truly a computer nerd: sitting there debating on the "effectiveness" of given system instead of just starting and making adjustments along the way.

The final kick in the pants was in November 2024  when I kept coming across in the media I consumed that I should get about the business of writing things down. From Cory Doctorow's [The Memex Method](https://pluralistic.net/2021/05/09/the-memex-method/) blog entry, Molly White's [Wind The Clock](https://www.citationneeded.news/wind-the-clock/) entry in her [Citation Needed](https://www.citationneeded.news/) newsletter, [Oxide And Friends](https://oxide-and-friends.transistor.fm/episodes)' podcast on [Technical Writing](https://oxide-and-friends.transistor.fm/episodes/technical-blogging) and following authors like [Michael W Lucas](https://io.mwl.io/@mwl) as well [Zig Zag Claybourne](https://wandering.shop/@zzclaybourne) on Mastodon, I realized I frankly needed to write.

So they have about 0.01% of the blame shared mostly equally, I think Michael W Lucas might hold the most since he forces me to pull out a dictionary to read his work.

Enough origin story, on the tools being used!
## Tools of MeekNotes Blog
#### Domain Host: Hover -  https://www.hover.com
I chose [Hover](https://www.hover.com) because it was the spot that could sell me the domain of meeknot.es. Fun fact: .es is the top level domain (TLD) for Spain in which I have some unverified ancestry claims to the Royal Court of Spain (maybe the family legends are true, maybe not). Past the fun fact, they have very simple domain redirects along with a simple DNS records interface for doing things like "I want to point my domain to this site". In the world where being a jerk to your customers is just another Tuesday, Hover has managed to not do this. The bar shouldn't be this low but I want to praise folks when they do good.
#### Static Site Host: Sourcehut Pages - https://sourcehut.org/
I use SourceHut for my Git hosting as I work to make GitHub my "if I have to" choice so it made sense to setup on their Pages offering since I am getting familiar with their ecosystem. I have a few gripes with GitHub that could be its own post but in short, I don't like the AI features they keep trying to sell me on and they feel big/bloated. In comparison, Sourcehut just works and does it without AI and without JavaScript! I have nothing major against these two technologies (AI and JavaScript) but it's cool to see someone do something different. Also [Drew DeVault](https://drewdevault.com/), who appears to be the most visible contributor/co-leader/person-in-charge of sourcehut, seems like an awesome, thoughtful software engineer.

Fair warning: SourceHut is in a public alpha but it has been rock-solid for me and happy to give them my money because I want to see them succeed. Sourcehut strikes me as a small quiet place of the internet so I am happy to come there and spend my time. Bonus points: a great little command line tool called hut and they have a path for self-hosting should I ever decide to do that. I will need to improve my homelabbing skills and equipment to pull that off.
#### Static Site Generator: Hugo - https://gohugo.io/
I have been using Hugo on and off now for the past 5 years and it has been simple enough for me to grok and understand. I have done some custom shortcodes in it to get Google Maps working for a friend's business site and some simple CSS tricks for a given theme. I love the fact that there are many themes for it and seems to have a solid community around it. I have yet to run into an issue with it.
#### Static Site Theme: Stack by Jimmy Cai - https://stack.jimmycai.com/
In keeping with the major theme of "staying out of Meek's way", this theme does that. It lets me just write and not worry about how to get everything configured. This theme includes plugins for comments should I want to turn that on at some point as well as great documentation on how to use different parts of the theme to make it my own. There's a nice copyright and set licensing for your articles built into the theme. Overall, it feels the right fit for my site right now: simple enough to get started but with some time and effort, I can add more without hurting my site or myself.
