---
layout: docs
title: Welcome
---

This site aims to be a comprehensive guide to COSMOS. We'll cover topics such
as getting your configuration up and running, developing test and operations scripts,
building custom telemetry screens, and give you some advice on participating in the future
development of COSMOS itself.

## So what is Ball Aerospace COSMOS, exactly?

COSMOS is a suite of applications that can be used to control a set of embedded systems. These systems can be
anything from test equipment (power supplies, oscilloscopes, switched power strips, UPS devices, etc), to
development boards (Arduinos, Raspberry Pi, Beaglebone, etc), to satellites.

### COSMOS Architecture

![COSMOS Architecture](/img/v5/architecture.png)

COSMOS 5 is a cloud native, containerized, microservice oriented command and control system. All the COSMOS microservices are docker containers which is why Docker is shown containing the entire COSMOS system. The green boxes on the left represent external embedded systems (Targets) which COSMOS connects to. The Redis data store contains the configuration for all the microservices, the current value table, as well as data streams containing decommutated data. The Minio data store contains plugins, targets, configuration data, text logs as well as binary logs of all the raw, decommutated, and reduced data. Users interact with COSMOS from a web browser which routes through the internal Traefik load balancer.

Keep reading for an in-depth discussion of each of the COSMOS Tools.

## Helpful Hints

Throughout this guide there are a number of small-but-handy pieces of
information that can make using COSMOS easier, more interesting, and less
hazardous. Here's what to look out for.

<div class="note">
  <h5>ProTips™ help you get more from COSMOS</h5>
  <p>These are tips and tricks that will help you be a COSMOS wizard!</p>
</div>

<div class="note info">
  <h5>Notes are handy pieces of information</h5>
  <p>These are for the extra tidbits sometimes necessary to understand
     COSMOS.</p>
</div>

<div class="note warning">
  <h5>Warnings help you not blow things up</h5>
  <p>Be aware of these messages if you wish to avoid certain death.</p>
</div>

<div class="note unreleased">
  <h5>You'll see this by a feature that hasn't been released</h5>
  <p>Some pieces of this website are for future versions of COSMOS that
    are not yet released.</p>
</div>

If you come across anything along the way that we haven't covered, or if you
know of a tip you think others would find handy, please [file an
issue]({{ site.repository }}/issues/new/choose) and we'll see about
including it in this guide.
