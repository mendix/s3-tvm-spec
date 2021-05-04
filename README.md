# S3 TVM Spec

This is an example API spec documentation if you wish to Implement TVM for [S3-Setting](https://github.com/mendix/cf-mendix-buildpack#s3-settings)


## Mendix Runtime >= 9.2
Mendix Runtime >= 9.2 now supports sts token for accessing s3 bucket so instead of creating an IAM user you can create an endpoint that can provide sts token to runtime.

## Mendix Runtime < 9.2
If you are using multiple Mendix Runtime Version and some of your environments are still using *Mendix Runtime < 9.2* you can enhance your tvm to provide IAM user credential instead of sts token.


Please check [s3-tvm-spec](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/mendix/s3-tvm-spec/main/s3-tvm.yaml) api doc for tvm endpoints.

* /v1/getcredentials: *Mendix Runtime <9.2*
* /v1/gettoken: *Mendix Runtime >= 9.2*