# Monitoring with AWS Cloud Watch
![](img/diagram.png)
![](img/diagram2.png)
# Auto scaling
## Step 1: Create a launch template
1. Open the [Amazon EC2 console](https://console.aws.amazon.com/ec2).

2. On the navigation bar at the top of the screen, select an AWS Region. The Amazon EC2 Auto Scaling resources that you create are tied to the Region that you specify.

3. In the left navigation pane, choose Launch Templates, and then choose Create launch template.

4. For Launch template name, enter my-template-for-auto-scaling.

5. Under Auto Scaling guidance, select the check box.

6. For Amazon machine image (AMI), choose a version of Amazon Linux 2 (HVM) from the Quick Start list. The AMI serves as a basic configuration template for your instances.

7. For Instance type, choose a hardware configuration that is compatible with the AMI that you specified (t2 micro).
*Alternatively, you can use a launch configuration to create an Auto Scaling group instead of using a launch template. For the launch configuration instructions, see [Create a launch configuration](https://docs.aws.amazon.com/autoscaling/ec2/userguide/GettingStartedTutorial.html#id-gs-create-lc).*

8. (Optional) For Key pair name, choose an existing key pair. You use key pairs to connect to an Amazon EC2 instance with SSH. Connecting to an instance is not included as part of this tutorial. Therefore, you don't need to specify a key pair unless you intend to connect to your instance.

9. Leave Networking platform set to VPC.

10. For Security groups, choose a security group in the same VPC that you plan to use as the VPC for your Auto Scaling group. If you don't specify a security group, your instance is automatically associated with the default security group for the VPC.

11. You can leave Network interfaces empty. Leaving the setting empty creates a primary network interface with IP addresses that we select for your instance (based on the subnet to which the network interface is established). If instead you choose to specify a network interface, the security group must be a part of it.

12. Choose Create launch template.

13. On the confirmation page, choose Create Auto Scaling group.
### Next Steps
- Launch an instance
- Create an Auto Scaling group from your template
- Create Spot Fleet
## Step 2: Create a single-instance Auto Scaling group

## Step 3: Verify your Auto Scaling group
## Step 4: Terminate an instance in your Auto Scaling group
## Step 5: Next steps
## Step 6: Clean up
# Load balancer