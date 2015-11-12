---
layout: post
title: USENIX Lisa 2015 - Conference Day One - Washington, DC
---

[![USENIX Lisa 15](/images/lisa15_banner_news.png "USENIX Lisa 15")](https://www.usenix.org/conference/lisa15)

### Opening Remarks

[SysAdmin1138 Expounds](http://sysadmin1138.net/)

### [Washington Marriott Wardman Park](http://www.marriott.com/hotels/travel/wasdt-washington-marriott-wardman-park/) ###
*2660 Woodley Road NW, Washington, DC 20008*

## One Year after the Launch of the U.S. Digital Service: What’s Changed?
9:00 am-10:30 am
Keynote Address
Mikey Dickerson, U.S. Digital Service

55 different comapnies involve with healthcare.gov from different states with poor communication.

Created a war room and setup monitoring which prior to that was not present. We learned that CNN has a 20-30 minute tape delay which they could determine by outages and when they showed up on CNN with them trying to log in.

Service hierarchy of needs: monitoring => incident response => post mortem/root cause analysis (RCA) => testing + release process => development => product

Averaged 17.5 hours a day for 9 weeks 7 days a week by December 12th and hired a bunch of folks and moved to the final war room #3.

Time Magazine article - Code Red (February 2014?)

Code for America - non-profit.

August 2011 - US Digital Service created.

Meet the Dishelved White House Staffer Who's Cleaning Up Government IT - ABC News

226 year long open source project with 535 commitors where flame wars frequently break out.  Not even Debian is this disfunctional though they are getting close with systemd

Lesson 1: The system does not care about your feelings.

You know you have a functioning buearcrary if it can create a response that no individual would want.

Lesson 2: Cruft you don't use can still hurt you. Take heartbleed the bug with its own logo!

Lesson 3: The older a system is, the harder it is to change.

The system for processing Medicaid claims is over 20 years old and written in Cobol that would take over 6 months to map out.  Its mostly maintained by a handful of employees who are mostly past retirement age.  It would still likely be easier to maintain rather then rewrite.  A rewrite even if perfectly execute would create hundred of changes.  Past a certain point, a rewrite isn't an option.  A rewrite of the United States is a revolution and I am not supposed to advocate that.

Lesson 4: Have to get past "root cause analysis."  Past a certain level of complexity, there is almost never just one cause of a problem.  Look up Nancy Leveson, MIT - http://sunnyday.mit.edu The discipline of "System Safety" or Fly-Fix-Fly

Healthcare.gov 2 - Electric Boogaloo - Was not news and often times that's the primary goal. After the second open enrolement, it cost $70 million just for the ID management piece with up to 25% error rate for it with a 5-8 seconds of max response time.  With a median number of 30 pages to click through but a max of 70.  SLS (back renamed as simple login system) now ID management costs $4 million, 0% error rate (4 errors in 100s of 1000s of logins) and .02 seconds of max response time.

Goal - Engage and educate potential college students of any age or background and those that support and advise them, to find schools best sutied to them.  College Score Card.  This isn't to rank Harvard and Yale #1 this year.  We are trying to get at the tremendous population of 1st generation college students looking at spending over $100k when there are so many schools that are not created equal.

The College Scorecard was built with human-centered design.  Every decision was informed by research and testing with students, parents and advisors.

College Scorecard - collegescorecard.ed.gov - Launched by the president on September 12, 2015..  Over 1 million users and 5 million page views.  At least 7 tools launched using Data API, including one in Spanish.

We are producing disabled veterans at a faster pace then we can process their claims.  There is a backlog of 7-8,000 applications waiting to be adjudicated of folks with serious injuries and likely with mental issues.  So Digital Service has been working on this quite a bit in the year.

Fast Company - Inside Obama's Stealth Startup (from last summer)

Web design standards - agencies are geting better about hiring compentent design firms but presently there are no standards.  Came up with the US Web Design Standards - playbook.cio.gov

Wired.com - New Standards Coule Make Government Sites Less Worthless

How dow we make sure nobody goes bankrupt (any more) under student loand debt?

How do we make srue we admit as many Syrian refugees as the law allows?

How do we make online identity secure enough for serious transactions?

How do we make criminal background checks faster and more reliable?

The Digital Services super family is around 180 or so folks.

Lookup  Admiral Grace Hooper's originial nanosecond. (in custody of US Naval History and Heritage Command)

www.whitehouse.gov/usds

### How Can You Scale It If You Don't Trust It?
11:00 am-11:45 am
Invited Talk
David N. Blank Edelman, Technical Evangilist Apcera

Production environments are all about trust.  What does the workload contain? where does it run? Are the right resources in play for the right workload for the right people? Can the information flow only in a secure manner?  The bigger the dploy, the harder it is to maintain the trust.  Super hard with multi-clouds.

policy - in general is a lot sexier! If you can do policy, you can let the machines do what they do best and people can do what people do best.  If your environment is setup such that you have to do things that can be automated you should be upset.

Where's your policy now?  You either have "the customs desk" where their job is usually to just say no as they vet requests causing delarys.  The other choice is "the wild, wild west" where anybody with a credit card can get whatever they want and things are spread out everywhere and eventually catches a stray bullet or a collapsed mine shaft.

What would be better? Make policy pervasive, explicit, and automatically enforced.

Pervasive means: resource limits (CPU, memory, etc), workload-to-workload connections (per port or protocol...automatic bidirectional trust is less secure), ingres/egress, external connectivity and routing, software commponets version control and deployment, log access, policy editing (who can read and write it), permissible operations between frontend and backend

What did I leave out?

  - Can I constrain affinity
  - Exception policy
  - What is the policy for changing policy
  - Policy compliance state
  - Cleaning policy?

You need to be able to scale, and you need trust to be able to do it.

www.apcera.com - dnb@apcera.com

One of the hardest parts about designing policy is usability and understandability.  If a developer is trying to get something done and cannot understand the policy it won't work.

### 5 Things You Might Not Know about NGINX
11:45 am-12:30 pm
Invited Talk
Shannon Burns, Developer Advocate for NGINX

NGINX

1. Compress assets for delivery
1. Stop form spamming
1. Load Balance WebSocket connections
1. NGINX is learning javaScript
1. NGINX now supports HTTP2

NGINX can Compress your data. you can use the gzip module with the key directives being gzip, gzip_type, and gzip_proxied.  Not to be used with binary content.  There is also the image filter module.

NGINX can stop brute fore retries.  You can use the HTTP limit req module.

NGINX supports WebSockets.

Now with nginScript.  Teaching our web server to speak browser.  Addressing the problem of developers wanting to change their application without changing code.  Custom JavaScript runtime.  Built for the server, not the browser.  Its not a replacement for LUA.  Just a module with the directives js_set and js_run.  Not a full Javascript implementation. Can be used as a bandaid to prevent known issues, control traffic, and extent the fuctionality of the application using microservices.  Still experimental.

NGINX now supports HTTP2.  You have to enable http2 and its still considered HTTP2.  It can affect optimizations so you will need to check application after enabling HTTP2

Be careful with gzip_proxied see Breach Attacks

### Getting Started with Puppet
2:00 pm-3:30 pm
Mini Tutorial
Thomas Uphill, Wells Fargo
@uphillian

Slides (watch in presentation mode for sweet animations) - https://docs.google.com/presentation/d/11t7XGsx9fDuhZ858PmZSJ8pFEyB61n2ea33SyCRM3O4/edit?usp=sharing

https://github.com/uphillian/lisa2015

/r/Puppet not /r/Puppetry

Alternatives - Ansible, CFEngine, Chef, DSC, Salt

Describe the state of the system not steps.  Idepotent.

RAL - Resource Abstraction Layer - abstract as a type (package) and have concrete resolution as providers (RPM, YUM, APT, Zypper)

Types - core types: file, packages, services, exec, mount, user, group...

Providers - Weight system for packages based on system type

Facter/Facts - Facter is a separate utility from Puppet such as ip address, architeture, fqwn, VM?, memory, selinux, etc.  Each of these facts can be used as variables in your puppet code.  Every time you run puppet, Facter runs first.  You can write your own facts in Ruby, Shell, Text, YAML.  In Puppet in 4.2.2, Facter is written in C++ as Ruby is really slow.  Presidence is done via a weighting system.  Custom facts usually weight higher though you can specify weight using Ruby facts.

Language - Based loosely on Ruby. A type with its attributes instantiated is a resource.  Those get stuffed into classes which define nodes.  You can have multiple classes in a module.  Any kind of Puppet code file is called a manifest and genarlly have the .pp file extension.  The catalog is the runbook/playbook, the compiled version of whats going on.

Classes create scope.  If you define a variable in a class, you can access it such as $class::variable.

Title of resources must be unique.  But the name vars can be the same. For name vars, the path is the name.

Only the unquoted true is true!  Only unquotes false is false!

Some discussion on using case vs the ternary operator selector and how you can use strings or regular expressions

Functions - include; altert,crit,debut,info,warning; each,map (Puppet); hiera; template; fail; define

docs.puppetlabs.com/puppet_core_types_cheatsheet.pdf

Files - 4 Ways to Create a Files

1. content
1. source
1. template ERB (Embed Ruby)
1. template EPP (Embedded Puppet in 3.8+)

What is configuring a system? Add packages, apply configuration files, start services which are covered by package, files, service

The compiled catalog is a JSON object

Metaparameters - ordering - before, require, notify, subscribe.  Other metas for apps - noop, stage (usually there is just the main stage but you can create other stages to run before or after main), schedule

Refer to an existing reource by capitalizing it.

DAG - directed acyclic graph - There are no loops as you need a place to start.

TURBOSPEED ENGAGE!

### Automated Security Compliance Evaluation of Your Infrastructure with SCAP
4:00 pm-5:30 pm
Mini Tutorial
Martin Preisler, Red Hat, Inc.

Slides - http://martin.preisler.me/wp-content/uploads/2015/11/USENIX-LISA15-Automated-Sec-Compliance-With-SCAP.pdf

SCAP Introduction

Security Content Automation Protocol - a NIST standard for expressing security policies with machine readable code.

https://nvd.nist.gov/scapproducts.cfm

11 certified vendors and several more support it but aren't certified yet

Two type of SCAP security policies: vulnerability assessment and security compliance.  How are my machines vulnerable? vs complying to specific rules.

Without SCAP you have manual compliance, BASH scripts or proprietary tools which have vendor lock-in

OpenSCAP is an open source implementation of SCAP 1.2

Goal 1: vulnerability assessment

Goal 2: Security compliance

BAIL!

### Working with Law Enforcement v3.0—Fifteen Years of Cooperation and Conflict
4:45 pm-5:30 pm
Invited Talk
Tom Perrine, Enterprise Architect - PlayStation, Sony Computer Entertainment

The rules:

1. Never talk about active cases
1. Always protect sources and methods
1. Always get competent legal guidance (probably not your legal department as they likely not trained in criminal law

Relationships matter
  - Know who to trust (people, not organizations)
  - Know who you may need and who may need you
  - You want to call Tier-3, not Tier 1
  - Play the long game

Have a plan

  - Know you goals - they may not be the same as law enforcement or the other related victims

Know your Criteria for Success

Remain Independent

Be Patient - investigations take months, cases take years, you are only seeing the tip of the iceberg

Be Kind

More then just hacking

Evidence - log like you mean it

Truth
