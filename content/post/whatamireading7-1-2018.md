---
title: "Things I stumbled upon this week"
date: 2018-01-06T22:32:29+11:00
---

## [Forget About Setting Goals. Focus on This Instead.](https://jamesclear.com/goals-systems)

I have always been a strong believer in setting goals to help team to focus. After reading this article and some recent experience, I realise this goal setting strategy doesnt work for all scenario. This article from James Clear really highlight some of the great point about why setting goals is not such a great idea sometimes. 

Depends on the challenges that a team is facing, I think employing the systems strategy is suitable for team where they need to develop good practises or habit. For example, establish a set of ground rule to facilate good programming practises and in a long run this good habit will help the team move faster as it produce more testable and maintainable code.

On the other hand, for team that has difficulty deciding on priority or keep switching between priority, having goal might be an effective way to help with decision making.

## Lambda 504 Gateway Timeout error

With more and more project using lambda, this week one of my colleague had some trouble with a lambda 504 gateway timeout error and I decided to do some more research about it.

This error happens when the lambda execution time exceed the maximum [non adjustable 29 seconds](https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html#api-gateway-limits) aws api gateway timeout. Although maximum execution time for lambda is 5 minutes but this is to accomondate the use of lambda with other aws services.

My default answer for this problem has always been _"I think we are using the wrong tool for the problem."_ Unfortunately there are times when we are forced to use lambda with api gateway so I decided to spend a bit of time to see if there is any recommended way of handling this situation.

Most of the [recommendation](https://github.com/serverless/serverless/issues/3171) talked about simplifying the lambda hence it can run different task in parrallel to reduce the process time. This [article](https://www.trek10.com/blog/lambda-fanout/) in particular described the fanout method to parallelise jobs in order to reduce time. These suggestions reminded me of the leader and follower pattern that was mentioned in the [SRE book](https://landing.google.com/sre/book.html) several time. With adequate monitoring and logging system, this is certainly a plausible approach.

As a bonus, also found this great [lambda architecture reference](http://www.allthingsdistributed.com/2016/06/aws-lambda-serverless-reference-architectures.html) article which I am sure will come in handy later. 

## [Biomimicry](https://99percentinvisible.org/article/biomimicry-designers-learning-natural-world/)

This word _Biomimicry_ popped up in my twitter feed the other day so I decided to go back to my podcast world and have a listen about it (since the word looks so cute). The podcast talked about the redesign of japanese bullet train, in particular using what we learn from the nature and apply that to the design. Now I am looking forward to read all about it in [this book](https://www.goodreads.com/book/show/432852.Biomimicry?ac=1&from_search=true)!
