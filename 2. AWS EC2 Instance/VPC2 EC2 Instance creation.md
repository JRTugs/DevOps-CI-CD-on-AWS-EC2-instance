# VPC2 - SonarQube, Nexus Repository, Prometheus/Grafana

## Creating 3 EC2 instances with the same resources, VPC and security group.

```bash
SPECIFICATIONS

Amazon Machine Image (AMI): Ubuntu Server 24.04
Instance Type: t2.medium
VPC1: 172.0.1.0/24
Storage: 15gb gp3
Keypair: Select the keypair that was created
```

**1. Creating EC2 instances**
  - On AWS Management Console, Click on the search bar and search for EC2
  - On the EC2 Dashboard on the left, Click Instances
  - On the top right, Click "Launch Instances"

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/e0e396ba-3c14-499c-a3bb-5642521f64cf)

  - On Launch an Instance Window, select the appropriate specifications.

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/8ea35ec5-3728-4fff-b721-04696987058a)

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/dbb3280d-303b-446e-a779-0ae29464cda0)

  - Click "Edit" to select VPC2

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/ef04617a-31e4-4c66-9c72-acbe63574b27)

  - Under Network Settings, Select the correct VPC, Subnet, Set Auto-assign IP to "Enable", Select existing security group and select the security group for VPC2

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/423ba2dd-958c-4b01-9803-ce8d12565fa8)

  - Under Configure Storage, change to 15 gb gp3
  - Once completed, Click on "Launch Instaces"

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/4b4ddda4-6fd0-49d2-8388-a990af81ad2f)

**2. Assign name for the Instances**

  - On Instances tab, Click the checkbox next to the instances and assign a name.

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/478e5c7e-0c6f-41f7-8109-8599938760a8)
