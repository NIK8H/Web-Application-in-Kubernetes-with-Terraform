### Give the IAM user Access to the Cluster
1.	Go back to the AWS Console's top Search bar, enter eks and select Elastic Kubernetes Service.
2.	Click the guru-eks- cluster you just deployed.
3.	Click the Access tab.
4.	In the IAM access entries section, click Create.
5.	In the IAM principal ARN field, enter and select eks-user
Leave everything else as is, including leaving the Type set to Standard.
6.	Click Next.
7.	From the Policy name drop-down, enter and select AmazonEKSClusterAdminPolicy.
Leave everything else as is, including leaving the Access scope set to Cluster.
8.	Click Add policy.
9.	Click Next.
10.	Scroll to the bottom of the page, and click Create.
The eks-user now has access to the cluster, and can issue awk eks and kubectl commands back at the command line.
11.	Back in the InstantTerminal browser tab, configure the Kubernetes CLI to use the cluster's context:
12.	aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)
Your session may have timed-out; if it has, issue the same ssh command you entered before.
13.	Confirm that the cluster is up and running:
14.	kubectl cluster-info
You should see that the Kubernetes control plane and CoreDNS are running as expected.

