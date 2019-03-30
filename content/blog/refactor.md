---
path: refactor
date: 2016-04-30T05:00:00.000Z
title: Refactor
---
If the classic programming book Code Complete had just one lesson, it’d be that great code is not born in the writing, but in the re-writing. He calls it refactoring, I call it ‘fixing shit’.

I have a definition for ‘great code’. It’s the state that a project reaches when the person or people maintaining it don’t have any nagging annoyances. No little tickles that this piece or that would be better structured a bit differently. No nagging feelings that the whole thing would have been better written a different way. No comments beginning with \`// TODO\`. Every questionable avenue has been explored, and it has been decided that the decisions made were the right ones.

One thing you’ll notice is this is all very dependent on what bugbears you happen to have. I might think my code is perfect, where you will find faults. Years of experience breed preferences which perhaps cannot be efficiently articulated, but are evidence of one solution to a problem being a bit better than another. This inconsistency has to be expected. It’s just not possible in the world of engineering to say if an idea is truly better. We can talk about it’s technical merits, we can point out key flaws, we can look to what’s most popular or most well regarded, but ultimately they’re all weak proxies for the ephemeral idea of ‘quality’.

So I leave it to each person to decide if the code they’re writing is ‘great’. Ultimately it’s not all that important, because so little code would be described that way anyway. Virtually everyone has peeves with the code they work on. If you work at any sort of established company or with almost any sizable codebase, you have things which you would do differently. It may in fact be so true that you don’t even think of these things anymore. The idea of having an entirely ‘designed’ environment is so far from reality it’s not even worth considering.

There are however, outposts. Projects which have been preciously maintained under watchful eyes. Every change considered. Huge swathes torn out when they were no longer needed, massive changes made when it became clear that there was a better way. I hesitate to name them, because it is always a matter of opinion, but many may ascribe these characteristics to projects like Haproxy, or parts of the Go standard librar.

These projects do have one defining characteristic. They are beloved. People call them reliable, logical, ‘easy once you get it’, consistent, complete.

So how do you get something that is logical? You can’t be afraid to make the changes when it becomes clear there was a simpler path. Rather than shoving in another argument to a function, you have to be willing and able to rework things. You have to be able to make changes.

So how can you make changes? Small projects, clearly defined interfaces, automated testing, well structured releases.

The final requirement is: small team. Very, very few people, preferably one, can be ultimately responsible for the project (or at least this part of the project). Many more can contribute through pull requests or patches, but at the end of the day, one single human must go to bed knowing he or she is responsible for the quality of this thing.

That feeling that the thing you are responsible for has an issue is the one and only motivation that can get someone to fix something that isn’t obviously broken to anyone else. And that type of change is exactly what you have to be willing to do if you want to end up with something great.

It should be clear that the pressures of most organizations are very much antithetical to writing great code. The idea of writing code when only the maintainer thinks it’s worth the time or even understands the purpose is not aligned with a project managers mindset. Depending on the size of your company, there are two solutions to this problem.

If you’re a startup, you’re in luck. Your engineers (probably you) very well may be your project managers (also you). It’s part of their job to prioritize ‘adding a Contact Us button’ against ‘rework how the cross-frame communication library works’. It only works when your engineers operate at a very high, product-focused, level. You can extend it a bit by putting as much control as is possible in the hands of your product engineers. PMs may decide what features should be worked on next, but engineers need to decide whether to work on those features, or a necessary backend improvement. Even then, management always applies pressure to release features and fix visible bugs. It takes a lot of isolation and a lot of responsible management.

It also requires the right breed of engineers. I don’t know why that is. It might be because engineers are traditionally not vested with this responsibility, so they don’t develop the skill. It could also be that it’s just not possible to disseminate all the information necessary to make informed product decisions to that many people. Finally, it might be that engineers are a selfish bunch and we will just end up doing whatever we want if given the freedom. It’s certainly possible to get lost down some pretty deep holes if you’re not careful.

As your organization grows, it becomes clear that the dividing lines between backend projects and parts of the product are far from the same. This starts to make ownership hard. It’s at this point that you might need to start siloing. Giving people the explicit responsibility of building infrastructure. Without the pressure to push product features, it’s possible for these engineers to focus on improving a tool or library. It goes without saying that ownership is critical. Open sourcing a project can go even further to create a the personal pressure necessary to keep a project great.

Building great software is hard for the simple reason that it’s almost always more exciting to add a feature or fix a bug than it is to fix how things are structured. The only way around this is to have a very personal connection with the code. Your ego must be tied up in it’s quality. Here are some things which destroy that connection:

* No one being responsible
* Too many people being responsible
* Managers or ‘experts’ making bad decisions about how things must go
* Bad languages or build systems which force developers to do things they know are wrong
* The feeling of impending doom (time pressure)
* Not knowing what the software is for, or why it needs to exist

A single craftsman will put his heart and soul into everything he builds because it’s a reflection of who he is. A large company will tend dissolve that kind of passion into numbers and opinions. If you want to build great things, you must find ways to create pockets of competence that are responsible for what they create.
