---
layout: post
title: "Who is your Brent?"
date: 2014-10-16 18:19:00 +0100
comments: true
author: Paul Devenney
categories: commentary books Phoenix Process
---
In the book [The Phoenix Project](http://www.amazon.co.uk/Phoenix-Project-DevOps-Helping-Business-ebook/dp/B00AZRBLHO/ref=sr_1_1?s=books&ie=UTF8&qid=1413480244&sr=1-1&keywords=the+phoenix+project) one of the primary foils of the "hero" is a guy named Brent. Brent is critical to successful work. Production incident? Call Brent. Complex database query? Brent's your guy. Tracing down network packet drops? Brent is already on it.  On the face of it, he is what every ops team wants twenty of, but as the book shows it is easy to become so critically dependent on one person that they become a bottleneck for the organisation. Also, Brent has several bad habits. He drops everything he's doing to sort out what ever is being screamed about loudest, regardless of its actual priority. He's also a knowledge silo - because Brent built half the complex systems in the business, he knows how to solve tricky problems with them all, but all the knowledge is in his head, to the point where most of the rest of the team won't touch those areas. Why would they? Brent can solve the issue in a tenth of the time, and more safely.

##Removing the Bottleneck
Much of the middle of the book is about how a mentor gets our hero thinking about how to remove that bottleneck. They tried hiring expensive experienced ops people. That failed because they still didn't have the knowledge of Brent, or if they gained it, it was also only in their heads. Part of the solution is to ensure that Brent is literally not allowed to touch the keyboard in production incidents, rather he must explain to a junior staff member how to step through the problems, and document the steps taken, and how to deal with the issue in future. The second part is ensuring visibility of all the work that Brent actually does, not just the stuff that was planned for him. This is one of the other key themes of the book - planned work vs unplanned work. 

##Unplanned Work
Unplanned work is a killer. Production incidents, sneaky off-the-books "can you just get something working for me" projects from senior management bypassing the project management / prioritisation functions, fixing another persons work because it's been "done wrong". Not only does it not appear on your projections of how well you are doing, but it also involves parking what you should be doing, called _context switching_, or leaving _work in progress_ (WIP). Gaining visibility of all the unplanned work Brent was doing was key to reducing that unplanned work. Sometimes this was even achieved by yelling at very senior management who were demanding that they "wanted Brent to look at the issue because he's the best", despite the fact that others were already doing that piece of work.

As Brent's unplanned work went down, it became possible to leverage his actual skillset in high value operations - such as early design review and planning. Without the fire-fighting he is able to take part in processes that reduce the amount of fire-fighting! A virtuous cycle indeed.

##A Person is not a workstation
In a twist in the later part of the book, the mysterious mentor points out to the hero, via manufacturing analogies, that a Brent is not a work centre or work station. That is, on on the macro level, a person is not a bottleneck, the function that they are carrying out is. In manufacturing you slow down your production of new work items to the speed where they can all be consumed by the next stage without queueing. One of these stations will be the slowest. That is your limiting factor or your bottleneck. (Note - a bottleneck does not specifically mean "bad". No matter how optimal your process gets _something_ will be the slowest part).

##Software Development Workstations
In the software development world, your "work stations" are things like requirements gathering, planning, architecture and design, implementation, code review, QA testing, deployment to an environment (including production or testing environments). Where is your limiting factor? What stage holds you up the most. One of the great messages in the book is (paraphrased) 

> Any improvements to a process that is not your bottleneck is a fake improvement

Basically - because WIP is so bad, anything that does not stop WIP building up at one cost centre is not really reducing the overall turnaround time for work from inception to successful production. You should _only_ focus on improving the bottleneck. When that is no longer the bottleneck, look to the next one.

##Identifying your Bottleneck
It's actually quite easy to do. Draw a diagram with a box for each process you have from requirements through to in production (generally a straight flow diagram). For each, identify whether they generally have a queue of items from the previous step. Now go from right to left until you find the first item that has a queue. That is your bottle neck. 

__Example__
> The average queue of stories in the backlog awaiting development work is about 15 items. The average number of stories awaiting QA is 5. The "quick" answer is to say that clearly the biggest problem is in development - they are coping least well! But think what would happen if you improved that part of the process. QA already has a queue of work - it would only get bigger. There is no point in resolving how much work development can process until QA is no longer the bottleneck.

As a real world reminder - here is an recent example from our own boards. You can see that we are building up a bottleneck on QA process. We've already gone through reviewing the underlying causes. We're tackling this area before re-assessing our next bottleneck.

{% img left /images/QA-bottleneck-example.png 500 750 'image' 'images' %}

##Conclusion
Where is your bottleneck? Who is your Brent? Find them and improve them first, because all other improvements are irrelevant!

