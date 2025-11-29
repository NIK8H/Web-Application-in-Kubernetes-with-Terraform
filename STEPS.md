### Create an IAM User and Configure the AWS CLI
>1. Use the lab's AWS Account credentials to log in to the AWS Console.
    Make sure you're in N. Virginia (us-east-1) region.

>2. In the AWS Console's top Search bar, enter and select IAM.

>3. On the left, click Users.

>4. In the upper-right, click Create user.

>5. For User name, enter eks-user, then click Next.

>6. Select Attach policies directly.

>7. Under Permission policies, select AdministratorAccess (check the box beside it), then at the bottom of the page click Next.

>8. Click Create user You've created the user under which you'll later deploy your EKS cluster.

>9. Click eks-user.

>10. Select the Security credentials tab, then click Create access key.

>11. Select Command Line Interface (CLI), and at the bottom check the I understand ... box, then click Next.

>12. Click Create access key.

>13. Under Secret access key click Show (to prevent a later pop-up).

>14. Copy both the Access key and Secret access key and store them locally for use later on.

Note: You would normally store this securely, in an encrypted password manager for example. This is not required for this lab.

>15. Click Done.

>16. On the lab page, expand the Cloud Server - Terraform Worker section, and copy the Password and Public IP for use next.

>17. Still at the lab page, click Instant Terminal, and at its command line enter the following, replacing <Public IP> with the Public IP you just copied.

ssh cloud_user@<Public IP>

`SSH`

![SSH ](<images/Main_Page_Images/Screenshot 2025-11-29 at 12.29.24 PM.png>)


>18. When prompted, enter y, and when prompted for a password, enter the Password you copied earlier.

>19. Configure the AWS CLI (Command Line Interface) so it can connect to your AWS instance as the eks-user your previously created:

aws configure

![alt text](</images/Main_Page_Images/image.png>)




>20. When prompted for the AWS Access Key ID, enter the Access key you stored earlier.

>21. When prompted for the AWS Secret Access Key, enter the Secret access key you copied from the AWS console.

>22. When prompted, press Enter twice to accept the Default region name, and then to accept Default output format.