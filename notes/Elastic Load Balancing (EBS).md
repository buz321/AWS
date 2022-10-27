## Elastic Load Balancing (EBS)
A load balancer acts as a single point of contact for all incoming web traffic to your Auto Scaling group. This means that as Amazon EC2 instances are added or removed in response to the amount of incoming traffic, these requests are routed to the load balancer first and then spread across multiple resources that will handle them.
