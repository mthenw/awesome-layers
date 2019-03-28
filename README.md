# λ AWSome Lambda Layers

**A curated list of awesome AWS Lambda Layers**

## What are Lambda Layers?

> Lambda Layers are a new type of artifact that can contain arbitrary code and data, and may be referenced by zero, one, or more functions at the same time. Lambda functions in a serverless application typically share common dependencies such as SDKs, frameworks, and now runtimes. With layers, you can centrally manage common components across multiple functions enabling better code reuse.

— https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-now-supports-custom-runtimes-and-layers/

## How to create and use Lambda Layers?

* [with Serverless Framework](https://serverless.com/blog/publish-aws-lambda-layers-serverless-framework/)
* [with SAM](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-template.html#serverless-sam-template-layerversion)
* [with AWS Console](https://aws.amazon.com/blogs/aws/new-for-aws-lambda-use-any-programming-language-and-share-common-components/)
* [with AWS CLI](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html) ([tutorial](https://github.com/nsriram/aws-lambda-layer-example)),
* [with Stackery](https://www.stackery.io/blog/lambda-layers/)

## Layers

### Runtimes

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| C++ (official) | Link: [awslabs/aws-lambda-cpp](https://github.com/awslabs/aws-lambda-cpp) | `provided` |
| Rust (official) | Link: [awslabs/aws-lambda-rust-runtime](https://github.com/awslabs/aws-lambda-rust-runtime) | `provided` |
| Bash | ARN: `arn:aws:lambda:<region>:744348701589:layer:bash:3`<br>Link: [`gkrizek/bash-lambda-layer`](https://github.com/gkrizek/bash-lambda-layer) | `provided` |
| [Crystal](https://crystal-lang.org/) | Link: [lambci/crambda](https://github.com/lambci/crambda) | `provided` |
| [Nim](https://nim-lang.org/) | Link: [lambci/awslambda.nim](https://github.com/lambci/awslambda.nim) | `provided` |
| Node.js v8 - N\|Solid | ARN: `arn:aws:lambda:<region>:800406105498:layer:nsolid-node-8:3`<br>Link: [accounts.nodesource.com/downloads/nsolid-lambda](https://accounts.nodesource.com/downloads/nsolid-lambda) | `provided` |
| Node.js v10 | ARN: `arn:aws:lambda:<region>:553035198032:layer:nodejs10:<version>`<br>Link: [`lambci/node-custom-lambda`](https://github.com/lambci/node-custom-lambda) | `provided` |
| Node.js v10 - N\|Solid | ARN: `arn:aws:lambda:<region>:800406105498:layer:nsolid-node-10:3`<br>Link: [accounts.nodesource.com/downloads/nsolid-lambda](https://accounts.nodesource.com/downloads/nsolid-lambda) | `provided` |
| Node.js v11 | ARN: `arn:aws:lambda:<region>:553035198032:layer:nodejs11:<version>`<br>Link: [`lambci/node-custom-lambda`](https://github.com/lambci/node-custom-lambda) | `provided` |
| PHP 7.1 | ARN: `arn:aws:lambda:<region>:887080169480:layer:php71:3`<br>Link:[`stackery/php-lambda-layer`](https://github.com/stackery/php-lambda-layer) | `provided` |
| Brainfuck | ARN: `arn:aws:lambda:<region>:444134189787:layer:brainfuck:1`<br>Built for fun, will not process events! | `provided` |
| LOLCODE | ARN: `arn:aws:lambda:<region>:444134189787:layer:lolcode:1`<br>Built for fun, will not process events! | `provided` |



### Utilities

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| GeoIP | Link: [`dschep/geoip-lambda-layer`](https://github.com/dschep/geoip-lambda-layer) | all |
| Git + SSH | ARN: `arn:aws:lambda:<region>:553035198032:layer:git:<version>`<br>Link: [`lambci/git-lambda-layer`](https://github.com/lambci/git-lambda-layer) | all |
| Puppeteer | ARN: `arn:aws:lambda:us-east-1:085108115628:layer:chrome:6`<br>Link: [`RafalWilinski/serverless-puppeteer-layers`](https://github.com/RafalWilinski/serverless-puppeteer-layers) | all |
| psycopg2  | Link: [`jetbridge/psycopg2-lambda-layer`](https://github.com/jetbridge/psycopg2-lambda-layer)  | `python3.6` `python3.7` |
| SQLite Python | Link: [`dschep/sqlite-lambda-layer`](https://github.com/dschep/sqlite-lambda-layer) | `python3.6` |
| Tesseract | Link: [`bweigel/aws-lambda-tesseract-layer`](https://github.com/bweigel/aws-lambda-tesseract-layer) | all |

### Monitoring

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| Datadog | ARN: `arn:aws:lambda:<region>:464622532012:layer:Datadog-Python36-metric:1`<br>Link: [Datadog's Lambda Layer](https://www.datadoghq.com/blog/datadog-lambda-layer/) | `python3.6` |
| Epsagon Node | ARN: `arn:aws:lambda:<region>:066549572091:layer:epsagon-node-layer:1`<br>Link: [Epsagon Node Layer](https://epsagon.com/blog/bring-your-epsagon-layer-to-aws-lambda/) | `nodejs6.10, nodejs8.10` |
| Epsagon Python | ARN: `arn:aws:lambda:<region>:066549572091:layer:epsagon-python-layer:1`<br>Link: [Epsagon Python Layer](https://epsagon.com/blog/bring-your-epsagon-layer-to-aws-lambda/) | `python2.7, python3.6, python3.7` |
| Thundra Java | ARN: `arn:aws:lambda:<region>:269863060030:layer:thundra-lambda-java-layer:1`<br>Link: [Thundra Java Layer](https://docs.thundra.io/docs/java-custom-runtime-and-layer-support) | `java8` |
| Thundra Node | ARN: `arn:aws:lambda:<region>:269863060030:layer:thundra-lambda-node-layer:1`<br>Link: [Thundra Node Layer](https://docs.thundra.io/docs/node-custom-runtime-and-layer-support) | `nodejs8.10` |

### Security
| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| PureSec | Link: [PureSec Lambda Protection Layer](https://www.puresec.io/blog/aws-lambda-security-with-zero-overhead-by-puresec) | `nodejs8.10` |
