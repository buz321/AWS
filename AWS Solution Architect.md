# AWS Solution Architect (plan to achieve in Jan 2023)

Aws Solution Architect

## VPC Endpoint
* AWS를 네트워크 안에서 EC2 인스턴스를 VPC 외부서비스와 private 하게 사용하기위해 쓰는것이다.
* 인터넷을 거치지 않음
* 동일한 리전에 있어야함
* 네트워크를 벗어나지 않기때문에 비용이 절감됨

## Reference:
https://explore.skillbuilder.aws


## Amazon Cognito

Amazon Cognito provides authentication, authorization, and user management for your web and mobile apps. Users can sign in directly with a user name and password, or through a trusted third party.

## Warm Standby

This solution meets the requirement for an RTO of 5 minutes. The instances run at a low capacity and can scale within minutes.

## Sticky Session (Application Load Balancer)

Sticky sessions use cookies to help the client maintain a connection to the same instance over a cookie's lifetime

## ECS vs EKS

## Cross-origin resource sharing (CORS)
Cross-origin resource sharing (CORS) defines a way for client web applications that are loaded in one domain to interact with resources in a different domain.

Which components are required to build a site-to-site VPN connection on AWS?
* Customer Gateway
* Virtual Private Gateway

### Amazon ECS and Aurora Serverless, they do not cost money when they are inactivate

## multipart upload to S3
You can use a multipart upload to upload larger files, such as the files in this scenario.


## Which command should a solutions architect run on the EC2 instance to gather the system metadata?
The only way to retrieve instance metadata is to use the link-local address, which is 169.254.169.254.
- 169.254.169.254.

## throttling limits (api gateway)
the burst limit represents the target maximum number of concurrent request submissions that API Gateway will fulfill before returning 429 Too Many Requests error responses.
