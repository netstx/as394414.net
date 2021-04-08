# as394414.net

## What?
- Static website for AS394414 using the [minimal theme](https://github.com/orderedlist/minimal) by [orderedlist](https://github.com/orderedlist).

## Where?
- [as394414.net](https://as394414.net) is hosted on AWS.

## How?
- DNS: Route53.
- GitHub: static website content in this repository.
- Hosting: CloudFront distribution with S3 bucket as origin.
- Automation: commits are automatically pulled into the S3 bucket using the AWS CodePipeline integration with GitHub Webhooks. Pipeline execution notifications are done with SNS+SES.

## Why?
- This is overkill for a single page static website, but I wanted to test some AWS features and I figured this was a good way to accomplish that.

## To-Do List:
- Use file versions in S3 so the CloudFront distribution refreshes more quickly after a commit is pulled from GitHub. Right now the cache settings are configured in the distribution itself, so it may take a while for latest commit to sync across all CloudFront edge locations. This would be more useful for sites that content is changed more often.

