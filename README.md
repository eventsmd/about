# What is my purpose?

![What is my purpose?](/img/purpose.jpeg)

There is no centralizaed way to get info about some outages in some governemnt and communal services, and of course, to subscribe to these ones that are concerning you by some parameters - by address of service provided, by name, whatever.

There are different sources - official websites, messanger channels where events for citizens are being published.

So the main idea is to collect it to one subscription based service that will notify you if everying is going to happen - water/electricity outage, there is a call you in court, there is closed road you go every day.

There was a successfull start with proof of concept with water outages and telegram bot to notify, sources are in the organization with cm_ prefix (communcal message).

# Architecture

![Scheme](/img/scheme.jpg)

There are planned list of parsers whatever it could be - water, electricity supplier, local government, courts, so on.

All of them will save all parsed messages to metadata storage and push it into the queue of processing - enrich geodata, transform plain text to json so underlying service can work with, and communcation gate via telegram bot in the start and a few frontends - web, telegram.
