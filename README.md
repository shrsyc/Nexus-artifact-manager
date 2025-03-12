# Maven CI/CD Pipeline with Nexus Repository

![nexus-pipeline](https://github.com/user-attachments/assets/17254150-22c2-4519-9268-e90645c1a9f8)

<br />
implemented a Jenkins CI/CD pipeline to automate the build and deployment process for a Spring Boot application using Maven and Nexus Repository.  

🔹 Automated pipeline workflow:  
✅ Checkout Source Code – Pulled the latest source code from GitHub using Jenkins.  
✅ Build & Validate with Maven – Executed mvn clean validate compile test package to ensure a reliable build.  
✅ Generate & Store Artifacts – Packaged the application as a .jar file.  
✅ Publish to Nexus Repository – Stored artifacts in two repositories:  
          - maven-releases (for stable production versions)  
          - maven-snapshots (for development versions, allowing multiple iterations). 

          
🔹 Key Technologies Used:  
☑️ Jenkins – Automating the CI/CD pipeline  
☑️ Maven – Dependency management and build automation  
☑️ GitHub – Source code management  
☑️ Nexus Repository – Storing and versioning artifacts  
☑️ Shell Scripting – Pipeline automation  
<br />
This setup ensures efficient version control, enabling seamless deployments and easy rollback to previous versions when needed. 🚀  

<br />

![nexus-repo](https://github.com/user-attachments/assets/c0548b7c-fb3e-4094-a45f-c1647ee65d1a)

