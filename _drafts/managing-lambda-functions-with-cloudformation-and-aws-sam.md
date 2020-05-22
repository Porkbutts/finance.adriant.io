---
layout: post
title: Managing AWS Lambda functions with CloudFormation and AWS Serverless Application Model
categories: aws
tags: lambda cloudformation sam
---

It's easy and convenient to get started with AWS Lambda by using the Console, but trying to manage multiple lambda functions via the in-browser editor for larger projects comes with its own set of limitations. Here are a few reasons why it's not advised to work exclusively in the in-browser editor.
- The browser could timeout while updating code and progress is lost.
- Lack of version control tooling like Git.
- Limits on deployment package size.
- Unable to install external package dependencies.

In an ideal environment, we develop and test our code locally and when we're ready we can package and deploy our code to AWS Lambda.

In order to get around these limitations, we'll learn how to manage and deploy lambda functions using [CloudFormation](https://aws.amazon.com/cloudformation/) and [AWS Serverless Application Model](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html) or *AWS SAM* for short.

Before we get started, this article assumes you already have some familiarity with the AWS CLI and understand the basics of Lambda functions. If not, check out my posts on [Getting started with the AWS CLI]({% post_url 2019-10-10-getting-started-with-the-aws-cli %}) and [Getting started with AWS Lambda]({% post_url 2019-10-20-getting-started-with-aws-lambda %}).

 <!--more-->

## What about AWS SAM?

## What about sam cli?
