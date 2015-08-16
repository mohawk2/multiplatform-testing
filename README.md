# Multi-platform Testing Infrastructure

## Introduction
This repo is for tracking the infrastructure-as-code that will enable **automated** multi-platform testing, specifically the multi-platform aspect of that.

The concept is to make a reproducible environment for a developer to run the same program automatically on a number of platforms (probably using virtual machines).

## Terminology
* wrapper: virtualisation wrapper (vagrant looks good for this)
* platform: an OS (or setup of an OS + other software: cf Cygwin) you want to test code on
* program: your code that you want to test on multiple platforms, almost certainly the automated test suite of your code
* deploy: getting your program gets onto each of your platforms
* run: running your program on each of your platforms

## Implementation plan
* identifying the best wrapper; currently this will be vagrant
* experimenting with the various VMs already available
* automating the creation of control files; currently Vagrantfiles
* automating the deploy process; initially with shell, later possibly Puppet
* automating the run process; this will probably follow on trivially once the deploy process works

## Resources
* Existing Vagrant boxes: http://www.vagrantbox.es/
* Getting a Solaris box dev-ready: https://github.com/PDLPorters/devops/issues/1
* Getting an OpenVMS vm running on Linux (in German): http://www.heise.de/ix/artikel/Dolly-Digital-1355065.html
