Copyright NetApp 2022. Developed by NetApp Solutions Engineering Team

Description: This Powershell script can be used to automate the integration of Netapp Fsx Ontap with Custom RDS (Relational Database Service) to allow Fsx Ontap to be used as a backend persistent storage for the database.

This template also integrates the Netapp Snapcenter software with Fsx Ontap to allow restore and backup of the data from Fsx.


Pre-requisites for running this template

- AWS Powershell Module should be installed on the host you run this script from

- Custom RDS Instance and SnapCenter server instance with IAM role that
 includes "ssm:SendCommand", "ssm:ListCommandInvocations" and
 "ssm:GetCommandInvocation" permissions along with the default permissions
 required for RDS (https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/custom-setup-sqlserver.html#custom-setup-sqlserver.iam-vpc)

- Custom RDS Instance, SnapCenter server Instance and Fsx Ontap should be able
 to communicate with each other (networking and security groups need to ensure the same)

- S3 Bucket with packages.zip, fsxLambdaFunction.zip, SnapCenter executable file and a pem file uploaded to it

- Fsx Ontap File System with NTFS-enabled SVM created along with Fsx and SVM
 passwords set
