# jq-layer
Amazon Linux 2023 JQ package for AWS Lambda layer use.
Binary and libraries are taken from a current Amazon Linux 2023 ARM64 (Graviton) instance.

_Note that this package includes the oniguruma shared libs. No further dependencies should be required to run `jq`on Amazon Linux 2023._
## Usage
Create a Lambda layer using the file `jq.zip`. Add that layer to your Lambda function.

### Architecture
When selecting architectures note that this package has been tested on Amazon Linux 2023 for arm64 (Graviton instances). It may also work on x86_64 but no testing has been done.
## Location of files
The binary will be installed under `/opt/bin` while all library files can be found under `/opt/lib`. Lamba functions should have `/opt/bin` in path.

## Using *jq*
You should be able to call `jq` from your function code without further modification to your environment.