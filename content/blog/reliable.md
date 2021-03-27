---
path: reliable
date: 2016-03-30T05:00:00.000Z
title: Reliable
description: "On reliability"
---
When a baby is removed from his or her mothers womb by a surgeon, the child springs to life. After nine months living on stolen oxygen, he or she starts breathing the moment air strikes.

In childbirth, hormones like Oxytocin spike in the mother's blood. They are used to prepare the mother for labor, and the baby for birth. But if they never come, the baby still breathes.

Our evolution did not forecast the development of obstetric surgery. Nor the development of space travel. Or of trips from our evolutionary home in Africa to the frigid north.

We are a reliable system. A system which survives. Reliable systems don't make assumptions about their environment beyond the minimum they need to survive. When the baby senses air he breathes. He doesn't wait for a hormone signal from the mother that labor is commencing.

In fact, we are much more reliable than most of the software systems we interact with. A human can be poked, prodded, cut and stabbed, and will keep right on working up to the moment of complete failure. Most computer programs will simply give up at the slightest tinge of error.

It is impossible to make a reliable mainframe. By mainframe, I am referring to a single monolithic machine, however large. It's impossible simply because math teaches us that if there is any chance a capacitor or memory chip will fail, given enough time, it will happen. The only path to reliability lies in numbers. Many machines, each willing and able to take up work to their ability. Should one fail, others take it's place. That is a reliable system.

But we already knew that. The cells of our body form the most numerous organism we can imagine. Trillions of little fungible automatons, each with their role, able to be lost without the slightest hiccup. Not only can we lose any cell, we are guaranteed to lose billions of cells every single day. A system which couldn't tolerate error wouldn't last very long.

Computers too get smart where the error rate get high. Memory incorporates error correcting codes similar to how proteins identify and fix errors in our DNA coding. The key difference though is what happens when that fails.

Cells are damaged by their environment, DNA is damaged by radiation, free radicals run amock destroying everything in their path. Most of this damage can be corrected. But sometimes, it is too severe. So the cell commits 'apoptosis', a technical term for suicide. It ends its life so that it might not kill it's neighbors or become cancer, and so that it's position can be taken up by a brother who might fare a bit better.

So where did we go wrong? Our reliability doesn't extend high enough. We designed systems which can handle failures of a bit or two of memory, but not ones which can handle failures of servers or data centers. And where we did design systems that handle failure, the handling requires careful coordination. This handholding is required because we see nothing more precious than the integrity of our data. We must always deploy a consistent, universal picture of the data in our system, lest all logic be lost.

The idea of a central store which gives all comers a consistent view of data is as old as the mainframe itself. When John Von Neumann was writing code for the 1024 words of memory contained in his IAS machine, he could be assured that if he wrote 5 to register 12, he could later read 5 from register 12. That principal formed the fundamental basis of imperative programming. But it's not how our body or brain works.

You cut your leg. It heals. How does that happen? How do your blood vessels know where to grow. How does your skin know where to start regrowing and when to stop?

Your blood vessel cells grow towards areas of low oxygen, like a plant bending toward the light (although the blood vessels grow anew). Without coordination, each cell is able to know which direction it is to grow by examining the oxygen gradient around it. Through that, they form the complex, beautiful webs of capillaries we all recognize.

Your skin cells know when to stop growing by 'contact inhibition'. When they bang into one another, they switch directions. If they bang into too many other cells, they stop moving. With that simple mechanism you end up with perfect, single layers of skin.

All of this is triggered by chemicals released when the original line of skin is destroyed. Those chemicals are sniffed by white blood cells to kill invaders, used by blood components to clot the flow, and sensed by nearby cells which migrate towards the source.

It may appear that there is a central authority involved, but there is not. Your brain does not look at your leg and say "Go heal this." The area seamlessly coordinates with millions of individual actors to accomplish a collective goal. To do so, it uses three methods which I'll give convenient (albeit simplified) names to:

## Gradients

Gradients are a value which naturally degrades along a path. For example, a gradient value could be lower the further away from Arizona a server was. The gradient value is different for every machine. In this case, it would represent how many miles away Arizona was.

## Contact

Contact is communication between individual nodes without use of a central arbiter. Nodes can be considered 'close' by any metric including physical location, latency, similarity of purpose, etc.

## Hormones

Hormones are general values exclusive to a location, or systemic within the system. For example, if more load is coming in than can be handled, the load balancer my release a 'stress' hormone. More machines may decide to launch in response to that increase, without explicit communication.

Like biological systems, building something like this which actually works would require a complex setup of action and reaction to prevent runaway conditions. It took evolution a hundred million years, it's unclear how hard it would be for us. But it would be reliable.
