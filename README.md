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

## How to share Lambda Layers publicly?

* [Tutorial with CLI examples](https://medium.com/@zaccharles/f1413b974f44)

## Layers

1. [Runtimes](#runtimes)
1. [Utilities](#utilities)
1. [Monitoring](#monitoring)
1. [Security](#security)

### Runtimes

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| C++ (official) | Link: [awslabs/aws-lambda-cpp](https://github.com/awslabs/aws-lambda-cpp) | `provided` |
| Rust (official) | Link: [awslabs/aws-lambda-rust-runtime](https://github.com/awslabs/aws-lambda-rust-runtime) | `provided` |
| Bash | ARN: `arn:aws:lambda:<region>:744348701589:layer:bash:<version>`<br>Link: [`gkrizek/bash-lambda-layer`](https://github.com/gkrizek/bash-lambda-layer) | `provided` |
| [Ballerina](https://ballerina.io/) | Link: [ballerina-platform/module-ballerinax-aws.lambda](https://github.com/ballerina-platform/module-ballerinax-aws.lambda) | `provided` |
| [Crystal](https://crystal-lang.org/) | Link: [lambci/crambda](https://github.com/lambci/crambda) | `provided` |
| [Nim](https://nim-lang.org/) | Link: [lambci/awslambda.nim](https://github.com/lambci/awslambda.nim) | `provided` |
| Node.js v8 - N\|Solid | ARN: `arn:aws:lambda:<region>:800406105498:layer:nsolid-node-8:<version>`<br>Link: [accounts.nodesource.com/downloads/nsolid-lambda](https://accounts.nodesource.com/downloads/nsolid-lambda) | `provided` |
| Node.js v10 | ARN: `arn:aws:lambda:<region>:553035198032:layer:nodejs10:<version>`<br>Link: [`lambci/node-custom-lambda`](https://github.com/lambci/node-custom-lambda) | `provided` |
| Node.js v10 - N\|Solid | ARN: `arn:aws:lambda:<region>:800406105498:layer:nsolid-node-10:<version>`<br>Link: [accounts.nodesource.com/downloads/nsolid-lambda](https://accounts.nodesource.com/downloads/nsolid-lambda) | `provided` |
| Node.js v12 | ARN: `arn:aws:lambda:<region>:553035198032:layer:nodejs12:<version>`<br>Link: [`lambci/node-custom-lambda`](https://github.com/lambci/node-custom-lambda) | `provided` |
| Perl 5.30.1 | ARN: `arn:aws:lambda:<region>:445285296882:layer:perl-5-30-runtime:5`<br>Link:[`shogo82148/p5-aws-lambda`](https://github.com/shogo82148/p5-aws-lambda) - see links to other version and [Paws](https://metacpan.org/pod/Paws) builds in repo | `provided` |
| PHP 7.1 & 7.3 | ARN: `arn:aws:lambda:<region>:887080169480:layer:php71:3`<br>Link:[`stackery/php-lambda-layer`](https://github.com/stackery/php-lambda-layer) | `provided` |
| PHP 7.2 & 7.3<br>cli & fpm | ARN: [`arn:aws:lambda:<region>:209497400698:layer:php-73:<version>`](https://runtimes.bref.sh/)<br>Link:[`brefphp/bref`](https://github.com/brefphp/bref) | `provided` |
| Pypy 3.5 | ARN: `arn:aws:lambda:<region>:146318645305:layer:pypy35:<version>`<br>Link: [IOpipe Pypy Layer](https://github.com/iopipe/lambda-runtime-pypy3.5) | `pypy3.5` |
| Brainfuck | ARN: `arn:aws:lambda:<region>:444134189787:layer:brainfuck:1`<br>Built for fun, will not process events! | `provided` |
| LOLCODE | ARN: `arn:aws:lambda:<region>:444134189787:layer:lolcode:1`<br>Built for fun, will not process events! | `provided` |
| Java 11 | Link: [andthearchitect/aws-lambda-java-runtime](https://github.com/andthearchitect/aws-lambda-java-runtime) | `provided` |
| Haskell | ARN: `arn:aws:lambda:<YOUR REGION>:785355572843:layer:aws-haskell-runtime:2` <br>Link: [Getting Started with the Haskell AWS Lambda Runtime](https://medium.com/the-theam-journey/getting-started-with-the-haskell-aws-lambda-runtime-951b2322c7a3) | `provided` |
| Swift | Link: [Amazon Linux Swift Layer](https://fabianfett.de/amazonlinux-swift) to be used with [swift-lambda-runtime](https://github.com/fabianfett/swift-lambda-runtime) | `provided` |


### Utilities

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| Apache Tika | ARN: `arn:aws:lambda:us-east-1:764866452798:layer:apache-tika:1`<br>Link: [`shelfio/apache-tika-lambda-layer`](https://github.com/shelfio/apache-tika-lambda-layer) | all |
| AWS CLI | Link: [`aws-samples/aws-lambda-layer-awscli`](https://github.com/aws-samples/aws-lambda-layer-awscli) | all |
| AWS Data Wrangler | Link:[`awslabs/aws-data-wrangler`](https://github.com/awslabs/aws-data-wrangler) ([`Releases`](https://github.com/awslabs/aws-data-wrangler/releases)) | `python3.6` `python3.7` `python3.8` |
| [better-sqlite3](https://github.com/JoshuaWise/better-sqlite3) | ARN: `arn:aws:lambda:us-east-1:284387765956:layer:BetterSqlite3:8`<br>Link: [`seanfisher/better-sqlite3-lambda-layer`](https://github.com/seanfisher/better-sqlite3-lambda-layer) | `nodejs12.x` |
| chrome-aws-lambda | ARN: `arn:aws:lambda:us-east-1:764866452798:layer:chrome-aws-lambda:4`<br>Link: [`shelfio/chrome-aws-lambda-layer`](https://github.com/shelfio/chrome-aws-lambda-layer) | all |
| ClamAV | Link: [`kindlyops/lambda-clamav-layer`](https://github.com/kindlyops/lambda-clamav-layer) | all |
| FFmpeg/FFprobe | ARN: `arn:aws:lambda:us-east-1:145266761615:layer:ffmpeg:4`<br>Link: [`serverlesspub/ffmpeg-aws-lambda-layer`](https://github.com/serverlesspub/ffmpeg-aws-lambda-layer) | all |
| GDAL + PDAL | Link: [`arn:aws:lambda:us-east-1:163178234892:layer:pdal:15`](https://github.com/PDAL/lambda) | all |
| GeoIP | Link: [`dschep/geoip-lambda-layer`](https://github.com/dschep/geoip-lambda-layer) | all |
| Ghostscript | ARN: `arn:aws:lambda:us-east-1:764866452798:layer:ghostscript:1`<br>Link: [`shelfio/ghostscript-lambda-layer`](https://github.com/shelfio/ghostscript-lambda-layer) | all |
| Git + SSH | ARN: `arn:aws:lambda:<region>:553035198032:layer:git:<version>`<br>Link: [`lambci/git-lambda-layer`](https://github.com/lambci/git-lambda-layer) | all |
| GraphicsMagick | ARN: `arn:aws:lambda:<region>:175033217214:layer:graphicsmagick:<version>`<br>Link: [`rpidanny/gm-lambda-layer`](https://github.com/rpidanny/gm-lambda-layer) | all |
| headless chromium with CJK fonts | Link: [`pahud/lambda-layer-headless-chromium`](https://github.com/pahud/lambda-layer-headless-chromium) | all |
| Headless PhantomJS | ARN: `arn:aws:lambda:us-east-1:699054759624:layer:phantom-js:4`<br> Link: [`shivtej1505/phantom-js-lambda-layer`](https://github.com/shivtej1505/phantom-js-lambda-layer) | all |
| Hugo | Link: [`jason-dour/hugo-aws-lambda-layer`](https://github.com/jason-dour/hugo-aws-lambda-layer) | all |
| kubectl for Amazon EKS | Link: [`aws-samples/aws-lambda-layer-kubectl`](https://github.com/aws-samples/aws-lambda-layer-kubectl) | all |
| LibreOffice | ARN: `arn:aws:lambda:us-east-1:764866452798:layer:libreoffice:7`<br>Link: [`shelfio/libreoffice-lambda-layer`](https://github.com/shelfio/libreoffice-lambda-layer) | all |
| libvips | Link: [`customink/ruby-vips-lambda`](https://github.com/customink/ruby-vips-lambda) Built for Ruby FFI but should work for all. | all |
| ModSecurity | Link: [`Zeerg/modsecurity-layer`](https://github.com/Zeerg/modsecurity-layer) | `python3.6` `python3.7` |
| MySQL PHP 7.1 | Link: [`aiir/php71-mysql-aws-lambda-layer`](https://github.com/aiir/php71-mysql-aws-lambda-layer) | [`stackery/php-lambda-layer`](https://github.com/stackery/php-lambda-layer) |
| Net-SNMP Tools | Link: [`jason-dour/net-snmp-aws-lambda-layer`](https://github.com/jason-dour/net-snmp-aws-lambda-layer) | all |
| OpenSSL | ARN: `arn:aws:lambda:us-east-1:034541671702:layer:openssl-lambda:1`<br>Link: [`alexandredavi/openssl-lambda-layer`](https://github.com/alexandredavi/openssl-lambda-layer) | all |
| OR-Tools | Link: [`matheusmessora/or-tools-layer`](https://github.com/matheusmessora/or-tools-layer) | `python3.6` |
| Pandoc | ARN: `arn:aws:lambda:us-east-1:145266761615:layer:pandoc:1`<br>Link: [`serverlesspub/pandoc-aws-lambda-binary`](https://github.com/serverlesspub/pandoc-aws-lambda-binary) | all |
| paramiko  | Link: [`jetbridge/paramiko-lambda-layer`](https://github.com/jetbridge/paramiko-lambda-layer)  | `python3.7` |
| PostgreSQL libpq | https://github.com/DrLuke/postgres-libpq-aws-lambda-layer | all |
| Puppeteer | ARN: `arn:aws:lambda:us-east-1:085108115628:layer:chrome:6`<br>Link: [`RafalWilinski/serverless-puppeteer-layers`](https://github.com/RafalWilinski/serverless-puppeteer-layers) | all |
| psycopg2  | Link: [`jetbridge/psycopg2-lambda-layer`](https://github.com/jetbridge/psycopg2-lambda-layer)  | `python3.6` `python3.7` |
| PySNMP | Link: [`jason-dour/pysnmp-aws-lambda-layer`](https://github.com/jason-dour/pysnmp-aws-lambda-layer) | `python3.6` `python3.7` `python3.8` |
| Python Toolkit | Link: [`keithrozario/Klayers`](https://github.com/keithrozario/Klayers)<br>Python packages incl. requests, aiohttp, pyOpenSSL etc.| `python3.7`|
| rsvg-convert | ARN: `arn:aws:lambda:us-east-1:145266761615:layer:rsvg-convert:2`<br>Link: [`serverlesspub/rsvg-convert-aws-lambda-binary`](https://github.com/serverlesspub/rsvg-convert-aws-lambda-binary) | all |
| SoX | ARN: `arn:aws:lambda:us-east-1:145266761615:layer:sox:1`<br>Link: [`serverlesspub/sox-aws-lambda-binary`](https://github.com/serverlesspub/sox-aws-lambda-binary) | all |
| SQLite Python | Link: [`dschep/sqlite-lambda-layer`](https://github.com/dschep/sqlite-lambda-layer) | `python3.6` |
| Tesseract | Link: [`bweigel/aws-lambda-tesseract-layer`](https://github.com/bweigel/aws-lambda-tesseract-layer) | all |
| Tex Live (LaTeX) | Link: [`https://github.com/serverlesspub/latex-aws-lambda-layer`](https://github.com/serverlesspub/latex-aws-lambda-layer) | `nodejs12.x, nodejs10.x, python3.8, java11` |
| Zip | Link: [`morugu/zip-aws-lambda-layer`](https://github.com/morugu/zip-aws-lambda-layer) | all |


### Monitoring

| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| Datadog | ARN: `arn:aws:lambda:<region>:464622532012:layer:Datadog-Python37:1`<br>Link: [Datadog's Lambda Layer](https://www.datadoghq.com/blog/datadog-lambda-layer/) | `python2.7, python3.6, python3.7`, |
| Epsagon Node | ARN: `arn:aws:lambda:<region>:066549572091:layer:epsagon-node-layer:1`<br>Link: [Epsagon Node Layer](https://epsagon.com/blog/bring-your-epsagon-layer-to-aws-lambda/) | `nodejs6.10, nodejs8.10` |
| Epsagon Python | ARN: `arn:aws:lambda:<region>:066549572091:layer:epsagon-python-layer:1`<br>Link: [Epsagon Python Layer](https://epsagon.com/blog/bring-your-epsagon-layer-to-aws-lambda/) | `python2.7, python3.6, python3.7` |
| Instana Node.js | ARN: `arn:aws:lambda:<region>:410797082306:layer:instana-nodejs:<version>`<br>Link: [Instana Node.js Layer](https://docs.instana.io/ecosystem/aws-lambda/nodejs/#the-instana-lambda-layers-for-nodejs-runtimes) | `nodejs8.10, nodejs10.x, nodejs12.x` |
| Instana Python | ARN: `arn:aws:lambda:<region>:410797082306:layer:instana-python:<version>`<br>Link: [Instana Python Layer](https://docs.instana.io/ecosystem/aws-lambda/python/#the-instana-lambda-layers-for-python-runtimes) | `python2.7, python3.6, python3.7, python3.8` |
| IOpipe Node | ARN: `arn:aws:lambda:<region>:146318645305:layer:IOpipeNodeJS810:<version>`<br>Link: [IOpipe Node Layer](https://github.com/iopipe/iopipe-js/releases) | `nodejs6.10, nodejs8.10` |
| IOpipe Python | ARN: `arn:aws:lambda:<region>:146318645305:layer:IOpipePython:<version>`<br>Link: [IOpipe Python Layer](https://github.com/iopipe/iopipe-python/releases) | `python2.7, python3.6, python3.7` |
| IOpipe Java | ARN: `arn:aws:lambda:<region>:146318645305:layer:IOpipeJava8:<version>`<br>Link: [IOpipe Java Layer](https://github.com/iopipe/iopipe-java/releases) | `java8` |
| Lumigo Node | ARN: `arn:aws:lambda:YOUR-REGION:724777057400:layer:lumigo-node-tracer:<version>`<br>Link: [Lumigo Node Layer](https://github.com/lumigo-io/lumigo-node) | `nodejs8.10, nodejs10.X` |
| Lumigo Python | ARN: `arn:aws:lambda:YOUR-REGION:724777057400:layer:lumigo-python-tracer:<version>`<br>Link: [Lumigo Python Layer](https://github.com/lumigo-io/python_tracer) | `python3.6, python3.7` |
| New Relic Node | ARN: `arn:aws:lambda:YOUR-REGION:451483290750:layer:NewRelicNodeJS810:<version>`<br>Link: [New Relic Node Layer](https://github.com/iopipe/newrelic-lambda-layers) | `nodejs8.10` |
| New Relic Node | ARN: `arn:aws:lambda:YOUR-REGION:451483290750:layer:NewRelicNodeJS10X:<version>`<br>Link: [New Relic Node Layer](https://github.com/iopipe/newrelic-lambda-layers) | `nodejs10.x` |
| New Relic Python | ARN: `arn:aws:lambda:YOUR-REGION:451483290750:layer:NewRelicPython27:<version>`<br>Link: [New Relic Python Layer](https://github.com/iopipe/newrelic-lambda-layers) | `python2.7` |
| New Relic Python | ARN: `arn:aws:lambda:YOUR-REGION:451483290750:layer:NewRelicPython36:<version>`<br>Link: [New Relic Python Layer](https://github.com/iopipe/newrelic-lambda-layers) | `python3.6` |
| New Relic Python | ARN: `arn:aws:lambda:YOUR-REGION:451483290750:layer:NewRelicPython37:<version>`<br>Link: [New Relic Python Layer](https://github.com/iopipe/newrelic-lambda-layers) | `python3.7` |
| Thundra Java | ARN: `arn:aws:lambda:<region>:269863060030:layer:thundra-lambda-java-layer:1`<br>Link: [Thundra Java Layer](https://docs.thundra.io/docs/java-custom-runtime-and-layer-support) | `java8` |
| Thundra Node | ARN: `arn:aws:lambda:<region>:269863060030:layer:thundra-lambda-node-layer:1`<br>Link: [Thundra Node Layer](https://docs.thundra.io/docs/node-custom-runtime-and-layer-support) | `nodejs8.10` |


### Security
| Name | ARN / Link | Compatible Runtimes |
|------|------------|---------------------|
| [Protego](https://protego.io/) | Link: [Protego Layers and Runtimes](https://www.protego.io/layers-and-runtimes-protego/) | `python2.7, python3.6, python3.7, nodejs6.10, nodejs8.10, java8, dotnetcore2.0, dotnetcore2.1` |
| [PureSec](https://www.puresec.io/) | Link: [PureSec Lambda Protection Layer](https://www.puresec.io/blog/aws-lambda-security-with-zero-overhead-by-puresec) | `nodejs8.10, nodejs6.10, python2.7, python3.6, python3.7, java8, dotnetcore2.x`|
