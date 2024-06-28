# Errors encountered when building the Jenkins Pipeline

## 1. Trivy not generating report
  - Checked Console Output log on build #2

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/35e079ab-92b4-4bd6-96a3-a94e4d0c4838)

  - Upon checking the console output log it seems it did not finish the file system scan

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/c52bff1d-6a59-42a1-b508-a501559e6a29)

  - Checked Jenkins server if it generated a trivy scan report and saw empty file

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/1f4cd1eb-19aa-4e70-9292-f417546d2aac)

**Solution:**
  - Updated Script
```bash
sh "trivy fs --format template --template '@/usr/local/share/trivy/templates/html.tpl' -o trivy-fs-report.html ."
```

# #2. SonarQube Analysis
  - SonarQube Analysis stuck
  - tried to check pipeline syntax and it seem not able to see the sonarqube instance

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/f1ed2cf2-626e-4167-9a8b-8b800883ea52)

  - SonarQube Servers under system is not configured

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/33dd4e34-823d-4b5b-8358-99fe6cae9115)

**Solution:**
  - Go to Manage Jenkins > System
  - Search SonarQube Servers and out the infromation

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/c042f818-408b-421b-9105-ff42ba68ba8a)
