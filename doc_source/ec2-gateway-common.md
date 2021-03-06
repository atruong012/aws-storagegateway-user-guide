# Deploying a Volume or Tape Gateway on an Amazon EC2 Host<a name="ec2-gateway-common"></a>

You can deploy and activate a volume or tape gateway on an Amazon EC2 instance\. Gateways hosted on Amazon EC2 instances can be used for disaster recovery and data mirroring\. The EC2 Amazon Machine Image \(AMI\) is available in the AWS Marketplace For volume gateway and tape gateways, we recommend using the **1\-Click Launch**\.

## Provisioning an Amazon EC2 Host by Using 1\-Click Launch<a name="ec2-gateway-onclick-tape"></a>

**To deploy a gateway on an Amazon EC2 instance**

1. On the **Select host platform** page, choose **Amazon EC2**\.

1. Choose **Launch with AWS Marketplace**\. You are redirected to AWS Marketplace where you launch the EC2 AMI\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/storagegateway/latest/userguide/images/host-ec2.png)

1. On AWS Marketplace, choose **Continue**\.

1. Choose **1\-Click Launch**\. Doing this launches the AMI with default settings\.

1. If this is your first time using an AWS Storage Gateway AMI, choose **Accept Terms** to accept the terms of service\.

1. Review the default settings\. You can accept and use these default settings or modify them to meet your needs\.

   The 1\-Click Launch feature comes with an autogenerated security group that is named AWS Storage Gateway\-1\-0\-AutogenByAWSMP\. For information about security group settings, see [Configuring Security Groups for Your Amazon EC2 Gateway Instance](Requirements.md#EC2GatewayCustomSecurityGroup-common)\.

1. After reviewing all your settings, choose **Launch with 1\-Click**\.

1. Choose **Return to Product Page** and locate your instance on the Amazon EC2 console\.
**Important**  
EC2 instances launched with the 1\-Click Launch functionality come with one root Amazon EBS volume\. You need to add additional EBS volumes to your instance as a separate step after the instance is launched\. For information about how to add EBS volumes, see [Attaching an Amazon EBS Volume to an Instance](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide//ebs-attaching-volume.html)\. 

1. In the Amazon EC2 console, choose your Amazon EC2 instance, choose the **Description** tab at the bottom, and then note the IP address\. You will use this IP address to connect to the gateway\.