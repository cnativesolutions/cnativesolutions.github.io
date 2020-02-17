---
layout: post
title:  "AWS Multi-Account Strategy"
description: Separate your workloads with multiple AWS accounts.
date:   2020-02-16 19:30:00 +0600
categories: aws
author: Azimov
---

Early AWS years a lot of companies made a bad choice by putting everything
in the same account. We will provide some information to explain why 
that was a bad choice.

![]({{site.baseurl}}/images/multi-account.png)

There are lots of benefits on having multiple AWS accounts. I will
try to write some of them here.

<h3>Having multiple AWS accounts is huge plus for security.</h3>
It provides great separation for your resources. You have flexibility on 
adding extra security layers to each account separately. 
Great for auditing purposes too. You could limit all the access to PCI account
or for backups account. You could prevent human error, there
will be very little chance of accidental deletion of resources.

<h3>Easy to deal with AWS resource limits.</h3>
AWS has hard and soft limits. With multi-account strategy you could
avoid hitting limits.

<h3>You can still combine them with AWS organizations.</h3>
It is very easy to combine all your accounts under one master account.
It gives you all the nice features to manage multiple accounts.
You can still benefit all the AWS offerings as they were one single account.

<h3>Great for billing purposes.</h3>
It is always nice to see where and how your AWS charges coming from.
Multiple accounts make it easy to see your bills. You can easily see
combined bill or per account. 

<h3>Basic multi-account strategy</h3>
At least you want to have following accounts.
1. Master account: billing, organizational account that manages all child accounts.
2. Logging account: You send all your logs. This allows you to keep your 
logs secure. Allows you to centralize all your logs. You can use various
log analytic tools to parse and use your logs.
3. Tooling account: Put all your CI/CD tools in this account.
4. Sandbox account: Having sandbox account is very important. 
You want everyone test their work in this account.
5. Development account: Initial development goes here.
6. Staging account: Every company names this account differently. 
Anyhow you want this account to reflect your production account.
7. Production account: Production account for end users.
8. Security account: All security tools go to this account. Where you can
scan other accounts and run different security tools.

There are companies I know use AWS account per team. There are companies have accounts
per product. You can have as many accounts as you want.
Having multiple AWS accounts is always better.