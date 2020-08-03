# as394414.net

## What
Simple static website for AS394414 using the [minimal theme](https://github.com/orderedlist/minimal) by [orderedlist](https://github.com/orderedlist).

## Where
[as394414.net](https://as394414.net) is hosted on my personal AWS account.

## How
- Domain: Route53
- GitHub: static website content in this repository
- Hosting: CloudFront distribution with S3 bucket as origin.
- Publishing: commits are automatically pushed to S3 using CodePipeline's integration with GitHub. Pipeline execution notifications are done with SNS+SES.

## Why
This is obviously overkill for a single page static website, but I wanted to test some AWS features and I figured this was a good way to accomplish that.
