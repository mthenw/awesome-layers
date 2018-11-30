# λ AWSome Lambda Layers

**A curated list of awesome AWS Lambda Layers** 

## What are Lambda Layers?

> Lambda Layers are a new type of artifact that can contain arbitrary code and data, and may be referenced by zero, one, or more functions at the same time. Lambda functions in a serverless application typically share common dependencies such as SDKs, frameworks, and now runtimes. With layers, you can centrally manage common components across multiple functions enabling better code reuse.

— https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-now-supports-custom-runtimes-and-layers/

#### How to create and use Lambda Layers?

* [with Serverless Framework](https://serverless.com/blog/publish-aws-lambda-layers-serverless-framework/)
* [with AWS Console](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-use-any-programming-language-and-share-common-components/)
* [with AWS CLI](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)

## Layers

| Name | Repo | Compatible Runtimes | ARN |
|------|------|---------------------|-----|
| PHP 7.1 Runtime | [stackery/php-lambda-layer](https://github.com/stackery/php-lambda-layer) | `provided` | `arn:aws:lambda:<region>:887080169480:layer:php71:3` |
| SQLite Python | [dschep/sqlite-lambda-layer](https://github.com/dschep/sqlite-lambda-layer) | `python3.6` | - | 
