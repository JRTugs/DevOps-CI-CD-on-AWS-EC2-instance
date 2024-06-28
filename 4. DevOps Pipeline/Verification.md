# Verfication

## Things you can check to verify deployment of Jenkins Pipeline

**1. Pipeline Stage View**

  - Jenkins Pipeline completed successfully

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/ad7db973-cb27-48f5-bea8-b21139a2d4e7)

**2. Website**
  - Most important is to check website is running
  - In this project, to access the website, I used http://IP:Port
  - Where IP = worker node public ip
  - Where Port = Port being used in kubernetes cluster

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/efcb4580-1f4b-4203-a561-637256cff4f1)

  - Running command in Kubernetes Master Node below will display port
    
```bash
kubectl describe service -n webapps
```

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/96b33b18-2a1a-4f91-9b2a-d080880cf5de)

  - Another way to get the port is in the console output
    
  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/88181635-708d-45f3-b383-b086933d6d6f)

**3. Dockerhub Repository**

  - Verify in dockerhub repository if image is updated every run of jenkins pipeline
    
  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/801a3c01-f0e7-4025-a787-e270e36ff138)

**4. SonarQube**

  -Checked SonarQube Analysis if updated and also check if there are bugs and vulnerabilities
  
  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/be7d59e2-2416-4b45-b1b0-757d181802f7)

**5. Nexus Repository**

  - Check Nexus Repository if package are being uploaded
    
  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/f416565c-d69f-48b7-a94a-2353ef758a9e)

**6. Trivy scan result**

  - Check Trivy scan result for both FS and Docker Image
  - Trivy scan result in this project is located in the /var/lib/jenkins/workspace/HelloWorld

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/548ae2ae-a628-4bfe-9784-5d38798b4b76)

**7. Kubernetes**

  - Check if kubernetes worker nodes are up and running and if number of replica is ok

  ![image](https://github.com/JRTugs/DevOps-CI-CD-on-AWS-EC2-instance/assets/29426766/6792bbf7-2637-49c4-9ce1-9a712b9de465)

