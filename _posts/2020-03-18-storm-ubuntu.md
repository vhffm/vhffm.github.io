---
layout: default
date: 2020-03-18
title: Install Apache Storm on Ubuntu 18.04 
---

### Install Java

$ sudo apt-get install openjdk-11-jre

$ sudo apt-get install openjdk-11-jdk-headless

$ sudo apt-get install maven

### Install Zookeeper

$ mkdir ~/bigdata

$ cd ~/bigdata

$ wget https://downloads.apache.org/zookeeper/zookeeper-3.6.0/apache-zookeeper-3.6.0-bin.tar.gz

$ tar xfvz apache-zookeeper-3.6.0-bin.tar.gz

$ cd apache-zookeeper-3.6.0-bin.tar.gz

$ cp conf/zoo_sample.cfg conf/zoo.cfg

Add two lines to conf/zoo.cfg:

![Zookeper Configuration](https://cheleb.net/public/images/storm_zkconf.png)

## Start Zookeeper

$ bin/zkServer.sh start

## Install Storm

$ cd ~/bigdata

$ wget ftp://apache.uib.no/pub/apache/storm/apache-storm-2.1.0/apache-storm-2.1.0.tar.gz

$ cd apache-storm-2.1.0

Add some lines to conf/storm.yaml:

![Zookeper Configuration](https://cheleb.net/public/images/storm_yaml.png)

## Start Storm

$ cd ~/bigdata/apache-storm-2.1.0

You may want to do all of the following in different tabs since the commands don't fork from (i.e., release) the shell.

$ ./bin/storm nimbus

$ ./bin/storm supervisor

$ ./bin/storm ui

After waiting a bit, you should be able to see the status UI at localhost:8080 in your browser.

![Zookeper Configuration](https://cheleb.net/public/images/storm_ui.png)
