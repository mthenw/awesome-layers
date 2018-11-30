# λ AWSome Lambda Layers

**A curated list of awesome AWS Lambda Layers** 

## What are Lambda Layers?

> Lambda Layers are a new type of artifact that can contain arbitrary code and data, and may be referenced by zero, one, or more functions at the same time. Lambda functions in a serverless application typically share common dependencies such as SDKs, frameworks, and now runtimes. With layers, you can centrally manage common components across multiple functions enabling better code reuse.

— https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-now-supports-custom-runtimes-and-layers/

## How to create and use Lambda Layers?

* [with Serverless Framework](https://serverless.com/blog/publish-aws-lambda-layers-serverless-framework/)
* [with AWS Console](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-use-any-programming-language-and-share-common-components/)
* [with AWS CLI](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)

## Layers

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| PHP 7.1 Runtime | ARN: `arn:aws:lambda:<region>:887080169480:layer:php71:3`<br>Link:[`stackery/php-lambda-layer`](https://github.com/stackery/php-lambda-layer) | `provided` |
| SQLite Python | Link: [`dschep/sqlite-lambda-layer`](https://github.com/dschep/sqlite-lambda-layer) | `python3.6` | 
| GeoIP | Link: [`dschep/geoip-lambda-layer`](https://github.com/dschep/geoip-lambda-layer) | all |
| Puppeteer | Link: [`RafalWilinski/serverless-puppeteer-layers`](https://github.com/RafalWilinski/serverless-puppeteer-layers) | all |
| Datadog | ARN: `arn:aws:lambda:<region>:464622532012:layer:Datadog-Python36-metric:1`<br>Link: [Datadog's Lambda Layer](https://www.datadoghq.com/blog/datadog-lambda-layer/) | `python3.6` |
| Thundra Java | ARN: `arn:aws:lambda:<region>:269863060030:layer:thundra-lambda-java-layer:1`<br>Link: [Thundra Java Layer](https://docs.thundra.io/docs/java-custom-runtime-and-layer-support) | `java8` |
| Thundra Node | ARN: `arn:aws:lambda:<region>:269863060030:layer:thundra-lambda-node-layer:1`<br>Link: [Thundra Node Layer](https://docs.thundra.io/docs/node-custom-runtime-and-layer-support) | `nodejs8.10` |
| Node.js v10 | ARN: `arn:aws:lambda:us-east-1:553035198032:layer:nodejs10:1`<br>Link: [`node-custom-lambda`](https://github.com/lambci/node-custom-lambda) | `provided` |
| Node.js v11 | ARN: `arn:aws:lambda:us-east-1:553035198032:layer:nodejs11:1`<br>Link: [`node-custom-lambda`](https://github.com/lambci/node-custom-lambda) | `provided` |
| Git + SSH | ARN: `arn:aws:lambda:us-east-1:553035198032:layer:git:2`<br>Link: [`Git Lambda Layer`](https://github.com/lambci/git-lambda-layer) | all |
