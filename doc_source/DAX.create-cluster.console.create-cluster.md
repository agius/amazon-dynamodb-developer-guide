# Step 2: Create a DAX Cluster<a name="DAX.create-cluster.console.create-cluster"></a>

Follow this procedure to create a DAX cluster in your default Amazon VPC:

1. Open the DynamoDB console at [https://console\.aws\.amazon\.com/dynamodb/](https://console.aws.amazon.com/dynamodb/)\.

1. In the navigation pane, beneath the **DAX** heading, choose **Clusters**\.

1. Choose **Create cluster**\.

1. In the **Create cluster** window, do the following:

   1. **Cluster name**—type a short name for your DAX cluster\.

   1. **Cluster description**—type a description for the cluster\.

   1. **Node type**—choose the node type for all of the nodes in the cluster\.

   1. **Cluster size**—choose the number of nodes in the cluster\. A cluster consists of one primary node, and up to nine read replicas\.
**Note**  
If you want to create a single\-node cluster, choose **1**\. Your cluster will consist of one primary node\.  
If you want to create a multi\-node cluster, choose a number between **2** \(one primary and one read replica\) and **10** \(one primary and nine read replicas\)\. 

   1. **IAM role**—choose **Create new**, and enter the following information:
      + **IAM role name**—type a name for an IAM role\. For example: *DAXServiceRole*\. The console will create a new IAM role , and your DAX cluster assume this role at runtime\.
      + **IAM policy name**—type a name for an IAM policy\. For example: *DAXServicePolicy*\. The console will create a new IAM policy, and attach the policy to the IAM role\.
      + **IAM role policy**—choose **Read/Write**\. This will allow the DAX cluster to perform read and write operations in DynamoDB\.
      + **Target DynamoDB table**—choose **All tables**\.

   1. **Subnet group**—choose the subnet group that you created in [Step 1: Create a Subnet Group](DAX.create-cluster.console.create-subnet-group.md)\.

   1. **Security Groups**—choose **default**\.

1. When the settings are as you want them, choose **Launch cluster**\.

On the **Clusters** screen, your DAX cluster will be listed with a status of *Creating*\.

**Note**  
Creating the cluster will take several minutes\. When the cluster is ready, its status changes to *Available*\.   
 In the meantime, you can proceed to [Step 3: Configure Security Group Inbound Rules](DAX.create-cluster.console.configure-inbound-rules.md) and follow the instructions there\.