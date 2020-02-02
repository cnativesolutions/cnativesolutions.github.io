---
layout: post
title:  "AWS Cost Optimization"
description: Basic steps to optimize your AWS costs.
date:   2020-02-01 19:30:00 +0600
categories: aws
author: Azimov
---

AWS bill is complex piece of the puzzle. AWS bill is a challenge for every single business.
Managing AWS cost could become a lot of work, if you do not take correct steps.
Especially, most people underestimate the data transfer costs.

![]({{site.baseurl}}/images/spot-usage.png)

Good thing is most of the suggestions come from AWS themselves. Unlike some other business providers, AWS 
wants you save money when you are using their platform. This is one of their strength as well. 
It is always nice as a customer to see honesty from the seller, it is natural. Looking at the AWS history,
you will notice they are doing improvements to their billing and cost savings.

What obvious steps you need to take to optimize your AWS bill?

1. First, do not use one AWS account for all your environments. Follow multi account strategy. 
Having many accounts has ton of benefits and helps with your AWS cost as well. We will write about this topic
later in detail.
2. Use tags, enforce tags! You can enforce billing tags from master account. Tags help 
you see detailed billing. We can talk about so much, but hey use tags.
3. Setup billing Cloudwatch budget alerts.
4. Setup billing reports.
5. Check out AWS Cost Explorer.
6. Have automation around on creating AWS resources. Try not to manually create resources from the console.
Use Terraform, Cloudformation, scripts and so on. In other words practice Infrastructure as a Code. 
7. Have automation around cleaning unused resources. This one is very important. You must check
and clean up unused resources. AWS does not care if you are utilizing the server or keeping it idle, they charge 
about the same amount of money.
8. Use AWS Spot Fleet where possible.
9. Try to leverage AWS serverless offerings. Now, they even offer serverless databases.
10. Purchase some Reserved resources for long running resources.
11. Don't use too many Availability zones. Most of the time 3 is more than enough. You will be
as fault tolerant with three Availability zones as you leverage seven.

List can go on and on. We will be writing more in detail on AWS cost savings in our future blog posts.
