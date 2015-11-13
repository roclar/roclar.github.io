---
layout: post
title: USENIX Lisa 2015 - Conference Day Three - Washington, DC
---

[![USENIX Lisa 15](/images/lisa15_banner_news.png "USENIX Lisa 15")](https://www.usenix.org/conference/lisa15)

### [Washington Marriott Wardman Park](http://www.marriott.com/hotels/travel/wasdt-washington-marriott-wardman-park/) ###
*2660 Woodley Road NW, Washington, DC 20008*

## Lean Configuration Management ##
9:00 am-10:30 am
Keynote Address
Jez Humble, VP, Chef @jezhumble

Takeaways

 - Throughput and stability are not a zero-sum game.  Going fast doesn't have to mean breaking things.  
 - culture => information flow => high performance
 - build quality in at the source.
 - systems engineering are doing product development

water- scrum- fall

[2015 State of DevOps Report](https://puppetlabs.com/2015-devops-report)

it performance

 - lead time for changes
 - release frequency
 - time to restore service
 - change fail rate

The same practices that allow you to more fast allow you to make corrections faster

Highest Correlation with IT Performance
[2014 State of DevOps Report](https://puppetlabs.com/2014-devops-report)

 - "Our code, app configurations and system configurations are in a version control system"
 - "We get failure alerts from logging and monitoring systems"
 - "Developers merge their code into trunk daily"
 - "When development and operations teams interact, the outcome is generally win/win"
 - "Developers break up large features into small, incremental changes."

Top Predictors of IT Performance

 - Peer-reviewed change approval process.  What chance is there that somebody who is never seen the code before can predict how changes will affect production?  Very little.  It just creates "Risk Management Theatre" of various pieces of the organization checking bureaucractic boxes.
 - Version control everything
 - Proactive monitoring
 - High trust organizational culture
 - Win-win relationship between dev and ops

[The Corporate Culture Survival Guide](http://www.amazon.com/The-Corporate-Culture-Survival-Guide/dp/0470293713)
[Your Startup is Broken: Inside The Toxic Heart of Tech Culture. Collected Essays by Shanley](http://model-view-culture.myshopify.com/products/your-startup-is-broken)

[New United Motor Manufacturing, Inc. (NUMMI)](https://en.wikipedia.org/wiki/NUMMI) A bad system will beat good people every time. How does your org deal with problems.  A good organization welcomes bad news so that they can fix the problems.

Failure should never lead to scape goating it should lead to investigation.

[A typology of organisational cultures](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1765804/) R Westrum

(Online Experimentation at Microsoft)[http://ai.stanford.edu/~ronnyk/ExPThinkWeek2009Public.pdf]

do less - "Evaluating well-designed and executred experiments that were designed to improve a key metric, *only about 1/3 were successful* at improving the key metric!"

[Impact Mapping](http://gojko.net/effect-map/) Gojko Adzic - "Impact Mapping facilitates the implementation of several techniques of agile planning, product design, prioritisation and scoping. In practice, I’ve found the combination of these techniques by far the most powerful way of iterative product management so far."

devops movement - A cross-functional community of practice dedicated to the study of building, evolving and operating rapidly changing, secure, resilent systems at scale

[Yes, you can really work from HEAD](http://queue.acm.org/blogposting.cfm?id=78323) Google does everything from trunk despite 10,000 devs across 40 offices.

[Large-Scale Continuous Testing in the Cloud](http://www.infoq.com/presentations/Continuous-Testing-Build-Cloud) - by John Penix on May 24, 2013

Build quality in - "Cease dependence on mass inspection to achieve quality.  Improve the process and *build quality into the product in the first place* -  W. Edwards Deming

Continuous testing is much better.  Its better to never check a bug in in the first place.

[Operations is a competitive advantage… Secret Sauce for Startups!](http://radar.oreilly.com/2007/10/operations-is-a-competitive-ad.html) Jesse Robbins

[Release It!: Design and Deploy Production-Ready Software](https://pragprog.com/book/mnee/release-it) - Michael T. Nygard

[Inside Amazon: Wrestling Big Ideas in a Bruising Workplace](http://www.nytimes.com/2015/08/16/technology/inside-amazon-wrestling-big-ideas-in-a-bruising-workplace.html) By JODI KANTOR and DAVID STREITFELDAUG. 15, 2015, NY Times

[Steve Yggve's Product Rant](https://plus.google.com/+RipRowan/posts/eVeouesvaVX)

[Early Amazon: Shopping cart recommendations](http://glinden.blogspot.com/2006/04/early-amazon-shopping-cart.html) - Greg Linden April 25, 2006

"I think building this culture is the key to innovation. Creativity must flow from everywhere. Whether you are a summer intern or the CTO, any good idea must be able to seek an objective test, preferably a test that exposes the idea to real customers.

Everyone must be able to experiment, learn, and iterate. Position, obedience, and tradition should hold no power. For innovation to flourish, measurement must rule."

[Old copy of the slide deck](http://www.slideshare.net/jezhumble/lean-configuration-management)

[Theory X and Theory Y](https://en.wikipedia.org/wiki/Theory_X_and_Theory_Y) - Your attitude towards the people who work for you will affect who works for you.

## Tools for Distributed (people), Open Source Systems Administration ##
11:00 am-11:45 am
Invited Talk
Elizabeth K. Joseph, HP @pleia2 [home page of Elizabeth Krumbach Joseph](http://princessleia.com/)

1. Out team
1. The OpenStack CI system
1. Code Review
1. Automated testing
1. Other collaboration tools
1. Communication

[Openstack Git Repo](http://git.openstack.org/cgit/openstack-infra)

[Openstack Dev Guide](http://docs.openstack.org/infra/manual/developers.html)

To make a change it goes to [Gerrit Code Review](https://code.google.com/p/gerrit/) then to [Zuul](http://status.openstack.org/zuul/), to Gearman to Jenkins then through the human code review.

Automated tests for infrastrucute: flake8 (pep 8 and pyflakes), puppet parser validate, puppet lint, Puppet application tests, XML checkers, alphabetized files, IRC Channel permissions

[OpenStack Cacti](http://cacti.openstack.org/) - Only sort of monitoring happening for OpenStack mostly due to resources available.

[Openstack Puppetboard](http://puppetboard.openstack.org/) - change tracking

[Openstack Project Infrastructure](http://docs.openstack.org/infra/system-config/)

Cannot do everything via git commits

 - Automation isn't perfect, sometimes you need to log in. Examples of Puppet agents falling over or database changes.
 - Complicated migrations and upgrades need manual components
 - Initial persisten server deployment still has manual components
 - Passwords need to be privately managed (but we use git!)

Maintenance collaboration on Etherpad (while also chatting on IRC with some use of [Pastebin](http://pastebin.com/)) - for example - https://etherpad.openstack.org/p/project-renames-November-6-2015

Human collaboration - Main IRC Channel (#openstack-infra) and other IRC channels.  [Channel/Meeting logs](http://eavesdrop.openstack.org).  [Pastebin](http://paste.openstack.org) logit.  In person collaboration at the OpenStack Design Summit every 6 months.  No voice or video calls.

Time zone issues can pose an issue.  Having folks in different regions increases coverage but first core member in a region struggles to feel cohesion, increased reluctance to land changes into production, makes for slow on-boarding.  Only solution seems to be to add more members in or near their region.

Goal is to expand Zuul to incorporate Jenkins functionality.

## Lightning Talks ##
11:45 am-12:30 pm
Lee Damon, University of Washington

Peter Ericksson - So I Joined a Startup, What Now?

Starups are usually setup by one person with a good idea that made money and thus resulted in a company that was organically grown.

You need to know is your mandate from senior management. 

Julie Gunderson - Power of a positive communitee

John Arrasjid - Choices Made Tied to Career Evolution

If you don't ask questions, for help, or for conference approval...When attending a conference, write a trip report.  What you expected to get out of, what you got out of it and how it applied to your job.  This will seed your request for following years.  Even if you feel uncomfortable speaking, make an effort.  Push your boundries.

Brian Sebby - Improvise a Lightning Talk

Metrics and visualization.  Prompt and response from the audience.

Stew Wilson - User Experience Uberalles

Find your 5 most common requests, determine the common missing interface and make sure the tickeing system always provides that information.  Then move to automation.

Chris Jones - Google Book Orielly Ornate Monitor Lizard by multiple engineers at Google

Andy Georges - Easy Build

Eric Logan - I Did Not Prepare for This

As sys admin, we are often thrust into stressful situations.  Often the adive is to not panic which doesn't seem useful.  When such a situation occurs, unless something is actually burning is to do nothing.  Take a moment to consider your course of action.  There are fast problems and slow problems.  The goal is to transform fast problems into slow ones where you can spend more time to investigate and also learn.  You likely aren't the first one to experience this problem.  Talk to co-workers and get Googling.

Deb Nicholson - GNU [MediaGoblin](http://mediagoblin.org/)

One of the only web based GNU projects.  We decentralize media hosting.  Organize around the individual rather then the media type.  Allows for more permissions and more difficult data discovery.

Stew Wilson - The Ux of You

Make it convenient to give up root by automating privileged tasks.

Aaron Dymond - The Small Epiphany He Had At His First LISA Conference

Ten years ago I taught high school Spaninsh, 5 years ago I went back to grad school, 3 years ago I was a MIDI professor.  I feel the need to start a support group for those who change careers.  Thank you all for your support and not judging me.  A year ago my lab didn't run.  It may still be a bit of a mess with my eight bosses.  But I am proud of my lab and I want to make sure it runs.

Julien Vehent - [sops demo](https://www.youtube.com/watch?v=YTEVyLXFiq0) 

Tool at Mozilla for managing secrets. There are project such as hiera, eyaml, etc but you always have to tailor these to your environment.  We needed something for encrypting YAML files.  [sops](https://github.com/mozilla/sops) can do this for us.

## Named Data Networking ##
2:00 pm-2:45 pm
Invited Talk
kc claffy, University of California, San Diego/CAIDA; Van Jacobson, University of California, Los Angeles

[Named Data Networking](http://named-data.net/) (NDN)

The fundemental idea of the telephone network is setup a point to point connection.  Fundementally, this wasn't changed via TCP/IP and RFC791.

NDN focuses on retrieving data from "the cloud".  Don't focus on where to get the data from.  Just focus on what data you want to get

Core protocls of The Net are decades old and were not designed to support the global internet.  Technically IP was an overall on the original phone network.

Stimulate innovation by addressing pain points:

 - Improve trust and security
 - Reduce complexity (and cost)
 - Enhance "fit" with applications
 - (and make it backward-compatible! think IP over leased lines, not 6to4)

First packet was sent over ARPAnet in 1969.

NDN is a new architecture based on lessons learned.  New communication, security and application development model.

NDN [Information Centered Networking](https://en.wikipedia.org/wiki/Information-centric_networking) (ICN) is much bigger then just content distribution.

All content must be signed.  Routers may, clients shall, verify.

Big idea:  Certificates are just named, signed data.

[Let's Encrypt](https://letsencrypt.org/) is a new Certificate Authority: It’s free, automated, and open.  In Limited Beta

Big Idea: Namespace design can convey capabilities, structure trust.

[Open mHealth](http://www.openmhealth.org/)

[NDN Github](https://github.com/named-data)

[NDN Tutorial](https://drive.google.com/folderview?id=0B6csWc5xquq-c3BLYS1YcnFQbGM&usp=sharing)

Tables:

 - PIT (Pending Interests Table)
 - FIB
 - CS (Content Store)

[Control Exchange Points: Providing QoS-enabled End-to-End Services via SDN-based Inter-domain Routing Orchestration](https://www.usenix.org/conference/ons2014/technical-sessions/presentation/kotronis)
[Geographic Routing Using Hyperbolic Space](http://www.cs.cornell.edu/~rdk/papers/pgr.pdf)

## Managing and Tracking Database Deployments ##
2:45 pm-3:30 pm
Invited Talk
CJ Estel, CoverMyMeds

[DBdeployer](https://github.com/covermymeds/dbdeployer)
[cjestel](https://github.com/cjestel)
[https://www.scriptscribe.org/](Scripts Scribe)

[CRUD](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) - Create, Read, Update and Delete
[DDL](https://en.wikipedia.org/wiki/Data_definition_language) - Data Definition Layer
[ETL](https://en.wikipedia.org/wiki/Extract,_transform,_load) - Extract, Transform, Load
