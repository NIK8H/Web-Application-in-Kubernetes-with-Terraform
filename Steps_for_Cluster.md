### Deploy the Cluster
>1.	Download the EKS Terraform configuration provided for the lab:
>2.	wget https://github.com/pluralsight-cloud/content-deploying-and-managing-a-web-application-in-kubernetes-with-terraform/raw/main/eks.zip
>3.	Once completed, list the files to ensure that it has downloaded:
>4.	ls
You should see the eks.zip file.
>5.	Unzip the file:
>6.	unzip eks.zip
>7.	List the files:
>8.	'ls'
You should now also see the eks directory.
>9.	Change into the eks directory:
>10.	cd eks
>11.	List the files in the directory:
>12.	ls
You should see the eks-cluster.tf, main.tf, outputs.tf, terraform.tf, variables.tf, and vpc.tf configuration files.
>13.	Initialize the working directory:
>14.	terraform init
>15.	Validate the configuration:
>16.	terraform validate
>17.	Apply the configuration and deploy the EKS cluster:
>18.	terraform apply
>19.	When prompted, enter yes to confirm.
Note: It can take between 10 and 15 minutes to deploy the cluster. Ensure that the deployment process completes successfully before moving on.

