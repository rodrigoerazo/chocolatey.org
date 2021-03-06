﻿Url: chocolatey-community-repository-issues-December-2019
Title: Chocolatey Community Repository - Service Interruptions
Author: The Chocolatey Team
Published: 20200115
Tags: chocolatey community, news, community repository, service availability
Keywords: community, community repository, chocolatey, news, intermittent issues
Summary: Community Repository has had numerous disruptions last month. Let's talk about it
---

If you are a regular user of the Chocolatey Community Repository, no doubt in the last few months you will have noticed that from time to time there were issues. You may have even ventured over to our [status page](https://status.chocolatey.org) and read over details of those issues. If you haven't noticed anything, well that has to do with the intermittent-ness of the issues.

**NOTE:** The direct use of the Chocolatey Community Repository is not recommended for organizational use. We recommend that you put in place a caching mechanism through the use of a “virtual repository” and cache packages when being installed for the first time. This will allow you to install a package many times without needing to reach out to the Community Repository more than once, although we recommend you look to [internalize packages instead to increase reliability](https://github.com/chocolatey/choco/wiki/how-to-host-feed). You can implement a Proxy Repository including the installation of a Repository Server, such as Nexus Repository Manager v3 (or NXRM v2) which automatically caches (but does not internalize) packages from the community repository, in around 15 - 30 minutes. We have video walkthroughs for [Nexus](https://www.youtube.com/watch?v=UehkG1VHtz0) and [Artifactory](https://www.youtube.com/watch?v=rMivH0DS9q8).

The popularity of Chocolatey Community has been huge, and that's thanks to all of you folks out in the community getting awareness out, helping out, and contributing Chocolatey packages! However, architecture that worked well for us in the past doesn’t work well when you double the number of requests that happen every day.

A year ago we were at 30 million requests per day! Per day! That's already a big success for the Chocolatey Community Repository. Yesterday we had 60.8 million requests. We’re humbled by what this means; we’ve doubled the popularity of the Chocolatey Community Repository in one year.

<img src="/content/images/blog/increased-web-traffic.png" alt="Increased Web Traffic" title="Increased Web Traffic" width="1100">

What worked well at 30 million requests per day, even 40 and 50 million requests per day, just doesn't quite work the same at 60 million requests per day. So we've been seeing some issues.

Over the past few months, the Chocolatey website, as well as the Chocolatey Community Repository, have been experiencing numerous intermittent service disruptions. Users have been reporting sporadic issues accessing both these resources. We take our commitment to the Chocolatey Community very seriously and wanted to take the time to give you all some context on the growing pains we are going through, and the steps we've taken so far to work on the issues:

* 21 SEP 2019 - Released the redesign of our front end website - a project that had been in the works for quite awhile! Some folks voiced usability concerns and we wholeheartedly jumped in and worked to meet those concerns over the next 3 months.
* 26 OCT 2019 - Migrated the database from third party host to our cloud infrastructure - adding beefier infrastructure to handle the next few years of growth.
* 25 NOV 2019 - First noticeable issues with timeouts.
* 25 - 27 NOV 2019 - Applying normal maintenance, as sometimes this is all that is necessary to fix issues with timeouts.
* 29 - 30 NOV 2019 - After coming to the realization that we need to find new bottlenecks and fix them with the growth stage, we started to work with consultants to help look over database and health to make suggestions on what we need to do outside of changes with code we start to look at implementing.
* 30 NOV - 08 DEC 2019 - Work on implementing aspects of those findings and deployed changes.
* 08 - 22 DEC 2019 - After learning those changes were not going to hold the issues, we moved into other areas to look at and continued to work through optimizations that could be completed. Monitored closely to see if those reduced impact or worsened and took appropriate action.
* 23 - 27 DEC 2019 - Monitor closely and restart when issues started to occur.
* 30 DEC 2019 - Met with consultants again to take another look into additional areas that needed to be addressed that would reduce/remove issues.
* 31 DEC - 02 JAN 2020 - Implemented changes that were able to be addressed in a short timeframe.
* 02 JAN 2020 - Deployed changes to site and continue to monitor for issues.
* 02 JAN - Today - Continue to monitor closely for residual issues / optimizations that need to be addressed.

<img src="/content/images/blog/request-latency.png" alt="Request Latency" title="Request Latency" width="1100">

Along with what we've done so far, let's also highlight where we are going with future plans:

* We are in the process of moving our infrastructure from a third party host to our cloud infrastructure, with the first phase of this completed in October 2019. Phase 2 will see the move of the rest of our infrastructure and is due to be completed by the end of Q1 2020.
* While the Chocolatey Community Repository and Website have extensive caching we are optimizing this caching to catch more requests. As part of Phase 1, we have already implemented more local caching that we continue to optimize. Going forward into Phase 2 we will be implementing further caching to improve responsiveness.
* In November 2018 we implemented rate limiting to improve the responsiveness of the website and it has served us well. Optimizing this limiting is an ongoing task, but we are seeing good results from this so far.
* The Chocolatey API is an area where we are currently focusing so we expect to see some optimization here soon without breaking any functionality.
* Along with the API, the Website is another area we’re focusing on. You can find those changes on [GitHub](https://github.com/chocolatey/chocolatey.org).

The rate of the increase in requests along with the massive growth in the Chocolatey team has come together to cause the perfect storm. It’s great that our community is showing their commitment to Chocolatey by supporting us with recommendations, blog posts, packages, among many other ways.

We’re grateful to our community for all your support, and we recognize that we have not communicated with you as we should; and for that, we apologize. We hope to do a better job at that going forward.

We also want to assure you that we take these issues seriously and have plans in place to rectify them, but it will take time. We ask for your patience and understanding as we work to resolve these issues and improve our services for you all. And most of all, we appreciate all your support. Our community is committed to Chocolatey and we are committed to our community.

Lastly, we would also like to acknowledge the hard work and dedication with which the Chocolatey Development and Operations teams came together, and worked tirelessly to return the Chocolatey Community Repository to a reliable state. Our resilience through this challenge has been a great learning experience, and we are fortunate to have had this opportunity to grow.