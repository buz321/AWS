# AWS Solution Architect (plan to achieve in Jan 2023)

Aws Solution Architect

## VPC Endpoint
* AWS를 네트워크 안에서 EC2 인스턴스를 VPC 외부서비스와 private 하게 사용하기위해 쓰는것이다.
* 인터넷을 거치지 않음
* 동일한 리전에 있어야함
* 네트워크를 벗어나지 않기때문에 비용이 절감됨

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

This can be used to solve microservice problems

### Amazon ECS and Aurora Serverless, they do not cost money when they are inactivate

## multipart upload to S3
You can use a multipart upload to upload larger files, such as the files in this scenario.


## Which command should a solutions architect run on the EC2 instance to gather the system metadata?
The only way to retrieve instance metadata is to use the link-local address, which is 169.254.169.254.
- 169.254.169.254.

## throttling limits (api gateway)
the burst limit represents the target maximum number of concurrent request submissions that API Gateway will fulfill before returning 429 Too Many Requests error responses.

## AWS Cognito
Amazon Cognito is designed for developers who want to add user management and sync functionality to their mobile and web apps. 

## Usage Plan

A usage plan specifies who can access one or more deployed API stages and methods—and optionally sets the target request rate to start throttling requests. The plan uses API keys to identify API clients and who can access the associated API stages for each key.

## AWS Transfer Family
AWS Transfer Family는 SFTP, FTPS, FTP 및 AS2 프로토콜을 사용하여 AWS 스토리지 서비스로의 반복적인 B2B 파일 전송을 안전하게 조정합니다.

## AWS Network Firewall
It is a stateful, managed network firewall and intrusion detection and prevention service for your virtual private cloud (VPC) that you created in Amazon Virtual Private Cloud (Amazon VPC). With Network Firewall, you can filter traffic at the perimeter of your VPC. This includes filtering traffic going to and coming from an internet gateway, NAT gateway, or over VPN or AWS Direct Connect.
<img width="1140" alt="스크린샷 2022-12-23 오전 7 00 45" src="https://user-images.githubusercontent.com/107760647/209233348-b1c9b7bf-fd80-49d0-8d36-3a8c2f0e0b16.png">


## AWS Firewall Manager
AWS Firewall Manager is a security management service that allows you to centrally configure and manage firewall rules across your accounts and applications in AWS Organizations.
<img width="999" alt="스크린샷 2022-12-23 오전 6 57 17" src="https://user-images.githubusercontent.com/107760647/209232951-22bc9cce-83ae-422a-a249-e2509b7b335b.png">

* AWS Network Firewall 랑 헷갈리지 말 것! 

## AWS Secrets Manager
a secrets management service that helps you protect access to your applications, services, and IT resources. This service enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.
* rotation 가능!!

## AWS Systems Manager
AWS Systems Manager centralizes operational data from multiple AWS services and automates tasks across your AWS resources. You can create logical groups of resources such as applications, different layers of an application stack, or production versus development environments.

## Reference:
https://explore.skillbuilder.aws
https://aws.amazon.com/ko/
