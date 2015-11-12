---
layout: post
title: USENIX Lisa 2015 - Conference Day Two - Washington, DC
---

[![USENIX Lisa 15](/images/lisa15_banner_news.png "USENIX Lisa 15")](https://www.usenix.org/conference/lisa15)

### [Washington Marriott Wardman Park](http://www.marriott.com/hotels/travel/wasdt-washington-marriott-wardman-park/) ###
*2660 Woodley Road NW, Washington, DC 20008*

## Sysadmins and Their Role in Cyberwar: Why Several Governments Want to Spy on and Hack You, Even If You Have Nothing to Hide ##
9:00 am-10:30 am
Keynote Address
Christopher Soghoian, Principal Technologist, American Civil Liberties Union

I explain technology and survalience to lawyers.

"I have nothing to hide" so why up my security?

You are targets, whether you like it or not.

Even if you have nothing to hide, you are still useful.

Governments with budgets in the billions are willing to compromise individuals who themselves have done nothing wrong in order to gain access to information they can get to as a means to an end.

Things you can do as somebody with access to make yourself a harder target:

 - Signal
 - Encrypt by default
 - Penetration resistent OSes such as [Qubes](https://www.qubes-os.org/)
 - The linux kernel team is focused on performance and reliability not as much on security. [The kernel of the argument](http://www.washingtonpost.com/sf/business/2015/11/05/net-of-insecurity-the-kernel-of-the-argument/) Microsoft took a lot of heat early on for being insecure but they have greatly advanced their security practices.  Linux needs to increase their kernel level security efforts as well.

## Docker Tutorial ##
11:00 am-12:30 pm
Mini Tutorial
John Willis, Docker - @botchagalupe

Dropbox Files - https://www.dropbox.com/s/ofxgoout0287ca8/Docker_Training%20-%20Base%20Copy.pdf?dl=0
GIST Files (Cheat Sheet) - https://gist.github.com/botchagalupe/53695f50eebbd3eaa9aa
Docker Book - http://www.dockerbook.com/
Docker Cookbook - http://shop.oreilly.com/product/0636920036791.do
The DevOps Handbook: How to Create World-Class Agility, Reliability, and Security in Technology Organizations Paperback – March 7, 2016
by Gene Kim (Author), Patrick Debois (Author), John Willis (Author), Jez Humble (Author), John Allspaw (Foreword) - http://www.amazon.com/The-DevOps-Handbook-World-Class-Organizations/dp/1942788002
Instructors docker.com posts - https://blog.docker.com/author/john-willis/

This is a one day class thats hard to fit into 3 hours.  The examples in the PDF are easy to do without instructor help.

OS Level Virtualization - Docker's class of virtualization

Realizing Linux Containers (LXC) - http://www.slideshare.net/BodenRussell/realizing-linux-containerslxc - Hypervisors vs containers

Docker Machine is a client for building Docker hosts.  Doc on installing it at http://docs.docker.com/machine/

Why Docker? Isolation, Lightweight, Simplicity, Workflow, and Community

Docker Client and Daemon of Docker Engine - docker version

Docker images are read only templates used to create containers which are isolated application platforms.

Registry (eg. Docker Hub) contain various repositories for images.

Docker installations are supported on my Linux platforms.  Installation script is available on https://get.docker.com  Note that if you use the default OS repositories you will likely get an older version.

To run docker commands without sudo you just need to add your user to the docker group.

Install Toolbox on Windows and Mac - https://github.com/docker/toolbox/releases

docker run does two things.  Creates the container using the image we specify and runs the container.  Has two important flags: -i to connect STDIN on the terminal and -t specifies to get a pseudo-terminal

docker exec is a much cleaner way to attach and detach from a docker container

docker inspect is how you get all of the metadata information for a container

## Automated Build and Deployment of Docker Hosts and Containers ##
2:00 pm-3:30 pm
Mini Tutorial
Bill Fraser and Dimitrios Liappis, Pythian @wmjfraser

https://github.com/pythian/lisa15-docker-tutorial

Pythian standard toolbelt in AWS: Auto Scaling Groups, CloudFormation template(s), Configuration Management (Puppet/Chef)

The Wrech was all environments including production must use Docker, Architecture must limit use of Amazone services, Ansible to be used for config management, Ansible Tower to be used for scheduling of tasks.

Deployment summary

 - Ansible tower and shipyard for orchestration
 - Ansible to deploy Docker images via Shipyard API
 - Consul for 

BAIL

## The Consilience Of Networking and Computing ##
4:00 pm-4:45 pm
Invited Talk
Dinesh G Dutt, Chief Scientist, Cumulus Networks
@ddcumulus

A while ago, networking and compute diverged causing us to need to solve problems twice.

[TensorFlow: smarter machine learning, for everyone](https://googleblog.blogspot.com/2015/11/tensorflow-smarter-machine-learning-for.html)

Structured I/O vs Myth of the Uniform Data Model

You can use Vagrant, Ansible (or you favorite configuration tool, and [Cumulus VX](https://cumulusnetworks.com/cumulus-vx/) to build a data center on your laptop.

## Vulnerability Scanning's Not Good Enough: Enforcing Security and Compliance at Velocity Using Infrastructure As Code ##
4:45 pm-5:30 pm
Invited Talk
Julian Dunn, Chef Software, Inc.

[Verizon 2015 PCI Compliance report](http://www.verizonenterprise.com/pcireport/2015/) - Key findings are 80% of companies fail at interim assessment right out of the gate.  From poor general hygeine patch management, dev security, log management/configuration,  or firewall configuration

The compliance tower of babel - Compliance speaks Excel, Security speaks in Shell, DevOps speak in code to manage systems.

[InSpec](https://www.chef.io/inspec/)

OpenSCAP is very good if you have a set of benchmarks you can already apply to your system.  InSpec is easier to read and write rules.

InSpec has very little to do with Chef and doesn't require configuration management.  It can be run locally on a machine or remotely.
