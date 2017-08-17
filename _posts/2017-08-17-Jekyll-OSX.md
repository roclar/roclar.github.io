---
layout: post
title: Jekyll and Mac OS X Sierra
---

Mac OS 10.12 (Sierra) does not have Ruby 2.1+ as of yet:

$ ruby --version
ruby 2.0.0p648 (2015-12-16 revision 53162) [universal.x86_64-darwin16]

So I have a bit of trouble getting Jekyll working.  Installing a few older versions got me going again:

    $ sudo gem install jekyll -v 3.4.5
    $ sudo gem install liquid -v 3.0.5
    $ sudo gem install bundler
    $ bundle install

Then I was able to run Jekyll normally.

The more correct way to address this problem though would be to use a more current version of Ruby.  [RVM](http://rvm.io/) allows for working with multiple Ruby environments.  Below are the steps I followed to get the local copy of my Jekyll site running.  I had to pick a directory that my user could read and write from to setup Homebrew during the installation.

    $ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
    $ curl -O https://raw.githubusercontent.com/rvm/rvm/master/binscripts/rvm-installer
    $ curl -O https://raw.githubusercontent.com/rvm/rvm/master/binscripts/rvm-installer.asc
    $ gpg --verify rvm-installer.asc
    $ bash rvm-installer stable
    $ rvm get head
    $ rvm autolibs enable
    $ rvm use --install 2.4.1 --create
    $ rvm list
        rvm rubies
        ruby-2.4.1 [ x86_64 ]

        # Default ruby not set. Try 'rvm alias create default <ruby>'.

        # => - current
        # =* - current && default
        #  * - default

    $ rvm use ruby-2.4.1
        Using ~/.rvm/gems/ruby-2.4.1
    $ gem install jekyll
    $ jekyll --version
        jekyll 3.5.2
    $ gem install bundle

Then in the site's project directory:

    $ bundle install

I also had to modify my $PATH setting so that RVM's bin directory was before where the system version of Jekyll was.
