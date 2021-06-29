---
title: "How to Contribute"
permalink: /docs/how-to-contribute/
modified: 2017-8-23T15:01:43-04:00
---

Apache RocketMQ is developed by an open and friendly community. Everybody is cordially welcome to join the community and contribute to Apache RocketMQ. There are several ways to interact with the community and to contribute to RocketMQ including asking questions, filing bug reports, proposing new features, joining discussions on the mailing lists, contributing code or documentation, improving the website, or testing release candidates.

{% include toc %}

## Ask questions!
The Apache RocketMQ community is eager to help and to answer your questions. We have a [user mailing list](/about/contact/) and [apache-rocketmq](https://stackoverflow.com/questions/tagged/rocketmq) tag on Stack Overflow.

## File a bug report
Please let us know if you experienced a problem with RocketMQ and file a bug report. Open [Github Issue](https://github.com/apache/rocketmq/issues) and click on the New issue. 

## Propose an improvement or a new feature

Our community is constantly looking for feedback to improve Apache RocketMQ. If you have an idea how to improve RocketMQ or have a new feature in mind that would be beneficial for RocketMQ users, please open an issue in [RocketMQ’s ISSUE](https://github.com/apache/rocketmq/issues). The improvement or new feature should be described in appropriate detail and include the scope and its requirements if possible. Detailed information is important for a few reasons:

* It ensures your requirements are met when the improvement or feature is implemented.
* It helps to estimate the effort and to design a solution that addresses your needs.
* It allow for constructive discussions that might arise around this issue.

Detailed information is also required, if you plan to contribute the improvement or feature you proposed yourself. Please read the Contribute [code guide](/docs/code-guidelines/) in this case as well.

We recommend to first reach consensus with the community on whether a new feature is required and how to implement a new feature, before starting with the implementation. Some features might be out of scope of the project, and it’s best to discover this early.

## Help others and join the discussions
Most communication in the Apache RocketMQ community happens on two mailing lists:

* The [user mailing lists](mailto:users@rocketmq.apache.org) is the place where users of Apache RocketMQ ask questions and seek for help or advice. Joining the user list and helping other users is a very good way to contribute to RocketMQ’s community. Furthermore, there is the [rocketmq](https://stackoverflow.com/questions/tagged/rocketmq) tag on Stack Overflow if you’d like to help RocketMQ users (and harvest some points) there.
* The [development mailing list](mailto:dev@rocketmq.apache.org) is the place where RocketMQ developers exchange ideas and discuss new features, upcoming releases, and the development process in general. If you are interested in contributing code to RocketMQ, you should join this mailing list.

You are very welcome to subscribe to both [mailing lists](/about/contact/).

## Test a release candidate

Apache RocketMQ is continuously improved by its active community. Every few weeks, we release a new version of Apache RocketMQ with bug fixes, improvements, and new features. The process of releasing a new version consists of the following steps:

1. Building a new release candidate and starting a vote (usually for 72 hours).
2. Testing the release candidate and voting (+1 if no issues were found, -1 if the release candidate has issues).
3. Going back to step 1 if the release candidate had issues otherwise we publish the release.
Our site contains a page that summarizes the [test procedure for a release](/docs/release-manual). Release testing is a big effort if done by a small group of people but can be easily scaled out to more people. The RocketMQ community encourages everybody to participate in the testing of a release candidate. By testing a release candidate, you can ensure that the next RocketMQ release is working properly for your setup and help to improve the quality of releases.

## Contribute code

Apache RocketMQ is maintained, improved, and extended by code contributions of volunteers. The Apache RocketMQ community encourages anybody to contribute source code. In order to ensure a pleasant contribution experience for contributors and reviewers and to preserve the high quality of the code base, we follow a contribution process that is explained in our Contribute [code guide](/docs/code-guidelines/). The guide does also include instructions to setup a development environment, our coding guidelines and code style, and explains how to submit a code contribution.

**Please read the Contribute [code guide](/docs/code-guidelines/) before you start to work on a code contribution.**

Please do also read the Submit a [Contributor License Agreement Section](http://www.apache.org/licenses/#clas).

Looking for an issue to work on?

We maintain a list of all known bugs, proposed improvements and suggested features in [Github issue](https://github.com/apache/rocketmq/issues).

## Contribute documentation

Good documentation is crucial for any kind of software. The Apache RocketMQ community aims to provide concise, precise, and complete documentation and welcomes any contribution to improve Apache RocketMQ’s documentation.

* Please report missing, incorrect, or out-dated documentation as a [Github issue](https://github.com/apache/rocketmq/issues).
* RocketMQ’s documentation is written in Markdown and located in the docs folder in RocketMQ’s [site source code repository](https://github.com/apache/rocketmq-site). See the Contribute [documentation guidelines](/docs/code-guidelines/) for detailed instructions for how to update and improve the documentation and to contribute your changes.

## Improve the website

The Apache RocketMQ website presents Apache RocketMQ and its community. It serves several purposes including:

* Informing visitors about Apache RocketMQ and its features.
* Encouraging visitors to download and use RocketMQ.
* Encouraging visitors to engage with the community.

We welcome any contribution to improve our website.

Please open a [Github issue](https://github.com/apache/rocketmq-site/issues) if you think our website could be improved.
Please follow the Improve the [website guidelines](https://github.com/apache/rocketmq-site) if you would like to update and improve the website.

## More ways to contribute…

There are many more ways to contribute to the RocketMQ community. For example you can

* give a talk about RocketMQ and tell others how you use it.
* organize a local Meetup or user group.
* talk to people about RocketMQ.
* …

## How to become a committer

Committers are community members that have write access to the project’s repositories, i.e. they can modify the code, documentation, and website by themselves and also accept other contributions.

There is no strict protocol for becoming a committer. Candidates for new committers are typically people that are active contributors and community members.

Being an active community member means participating on mailing list discussions, helping to answer questions, verifying release candidates, being respectful towards others, and following the meritocratic principles of community management. Since the “Apache Way” has a strong focus on the project community, this part is very important.

Of course, contributing code and documentation to the project is important as well. A good way to start is contributing improvements, new features, or bug fixes. You need to show that you take responsibility for the code that you contribute, add tests and documentation, and help maintaining it.

Candidates for new committers are suggested by current committers or PMC members, and voted upon by the PMC.

If you would like to become a committer, you should engage with the community and start contributing to Apache RocketMQ in any of the above ways. You might also want to talk to other committers and ask for their advice and guidance.

## Reference

This document is a modified version of the one created by the Flink Project[1].

[1]. http://flink.apache.org/how-to-contribute.html
