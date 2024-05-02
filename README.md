Difference between stopping and terminating an EC2 instance:
Stopping an EC2 instance halts its operation and preserves its data on the instance's root volume. You can start the instance again later.
Terminating an EC2 instance permanently deletes it along with its associated data. Once terminated, the instance cannot be restarted.
Adding an existing instance to a new Auto Scaling group:
You cannot directly add an existing instance to a new Auto Scaling group. Auto Scaling groups manage the lifecycle of instances, including launching new ones and terminating old ones based on defined policies. To incorporate an existing instance into an Auto Scaling group, you typically create a new launch configuration or use an existing one, then update the Auto Scaling group to use that configuration. This process involves specifying the instance ID and other configuration details.
Configuring CloudWatch to recover an EC2 instance:
You can configure CloudWatch to monitor the health of EC2 instances and trigger actions based on predefined alarms. To recover an EC2 instance automatically, you can create CloudWatch alarms that monitor metrics such as CPU utilization, network traffic, or custom application metrics. When these metrics exceed or fall below specified thresholds, CloudWatch can trigger actions, such as terminating the unhealthy instance and replacing it with a new one.
Difference between Latency Based Routing and Geo DNS:
Latency Based Routing: Routes traffic to the AWS region with the lowest latency for the end user. It measures the round-trip time (RTT) between the user and each region to determine the optimal routing.
Geo DNS: Routes traffic based on the geographic location of the user's DNS resolver. It maps users to specific servers or locations based on their geographic location.
How Amazon Route 53 provides high availability and low latency:
Route 53 achieves high availability and low latency through:
Global anycast routing: Distributes DNS queries across multiple geographically dispersed servers to reduce latency and increase fault tolerance.
Health checks: Continuously monitors the health of endpoints and routes traffic away from unhealthy ones.
Traffic flow: Enables sophisticated routing policies to direct traffic based on various factors such as latency, geography, and endpoint health.
Difference between a Domain and a Hosted Zone:
Domain: A human-readable name that represents a website or application, such as example.com.
Hosted Zone: A DNS database hosted on Route 53 that maps domain names to IP addresses. It contains records such as A, AAAA, CNAME, and MX records.
Elements of an AWS CloudFormation template:
Resources: Defines the AWS resources to be created or managed.
Parameters: Allows users to input custom values when creating or updating stacks.
Outputs: Exports values from the stack for use by other stacks or applications.
Conditions: Defines conditional logic for resource creation.
Metadata: Provides additional information about the template.
Transform: Applies AWS CloudFormation macros or other transformations to the template.
What happens in CloudFormation when one of the resources in a stack cannot be created successfully:
CloudFormation rolls back the entire stack to its previous state, ensuring consistency and preventing partial deployments. It then provides details of the failure, allowing users to troubleshoot and address the issue.
Steps involved in a CloudFormation Solution:
Design the architecture: Define the infrastructure components and their relationships.
Create a template: Write a CloudFormation template describing the desired resources and their configuration.
Launch the stack: Deploy the template to AWS, which creates the specified resources.
Monitor and manage: Use AWS Management Console or APIs to monitor the stack's status, update resources, and handle any issues that arise.
