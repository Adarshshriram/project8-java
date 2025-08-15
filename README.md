# project8-java

# Simple Java Maven Build with Jenkins

# Objective

- Run a simple Java Maven build job in Jenkins to understand Continuous Integration basics.

# Tools Required

- Jenkins (installed via Docker)
- Java JDK 8 or 11
- Maven
- Git

# Step-by-Step Guide

**1. Clone the Project from GitHub**

 - git clone < reository link >

**2. Start Jenkins (via Docker)**

- docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

**3. Configure Jenkins**

- Go to Manage Jenkins → Global Tool Configuration
- Add:
  - JDK (e.g., Java 11)
  - Maven (e.g., Maven 3.8.6)
- Save

**4. Create Jenkins Freestyle Job**

- New Item → Name: java-maven-build
- Freestyle Project
- Source Code Management: Select Git → Add Repo URL
- Build: Select "Invoke top-level Maven targets"
- Goals: clean package
- Save

**5. Build & Verify**
 
- Click Build Now
- Open Console Output → You should see:

  - [INFO] BUILD SUCCESS

# Sample Output Screenshot

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/8fd9736a-5b82-46e4-8f93-cf96fab9683b" />

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/c348a998-1c5d-4e66-b08c-f1d42fade068" />


# Key Learnings

- How Jenkins integrates with Maven
- How to run builds from a Git repository
- Understanding Jenkins console logs
