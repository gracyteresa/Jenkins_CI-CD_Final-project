# Hotstar Clone – CI/CD Pipeline using Jenkins

**Project Overview**
This project demonstrates an end-to-end CI/CD pipeline using Jenkins to automate the build, code quality analysis, artifact management, and deployment process.
I used a static Hotstar clone project as the source code and implemented a complete CI/CD workflow.

⚙️ **Workflow**

Source Code(github): Static Hotstar web files stored in GitHub.                     
Build(maven): Packaged using Maven to generate a .war file.
Code Quality Check(sonarqube): Integrated with SonarQube for static code analysis.
Artifact uploading(nexus): Uploaded the generated .war file to Nexus Artifactory.
Deployment(tomcat-server): Automatically deployed the artifact to a Tomcat server using Jenkins

**PLUGINS USED:** 
1. Deploy to container                                                                                                                          
2. Nexus artifact uploader 
3. Sonarqube scanner 
4. Sonarqube server 
5. Pipeline stage view

Sonarqube
<img width="903" height="283" alt="image" src="https://github.com/user-attachments/assets/a2a112e6-212a-40d7-9ba4-933a76413403" />
Nexus
<img width="903" height="244" alt="image" src="https://github.com/user-attachments/assets/4ff4806a-f409-4924-ba80-ceaff7a3ad2e" />
Tomcat server-hotstar clone
<img width="903" height="382" alt="image" src="https://github.com/user-attachments/assets/8de54a38-8b63-4f31-b13e-9288fff71ddc" />
Jenkins Pipeline
<img width="578" height="232" alt="image" src="https://github.com/user-attachments/assets/5f3be01e-4ff2-4d12-bf22-b38c5f374ce9" />




