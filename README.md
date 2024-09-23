Step 1: Install SonarQube Scanner on Jenkins

  1.Install the SonarQube Scanner Plugin:

Go to Jenkins Dashboard > Manage Jenkins > Manage Plugins.

Search for SonarQube Scanner in the Available tab.
Install the plugin and restart Jenkins if required.
Configure SonarQube in Jenkins:

Go to Jenkins Dashboard > Manage Jenkins > Configure System.
Scroll down to the SonarQube servers section.
Click on Add SonarQube.

![image](https://github.com/user-attachments/assets/35c2ffaf-a8c5-4817-ad3a-be0b03f1733b)


     Enter the Name, Server URL, and authentication token.
        
        1. Name:  A name to identify this SonarQube server.
        2. Server URL: URL of your SonarQube server (e.g., http://your-sonarqube-server).
        3. Authentication Token: Use the token credential ID sonar_token 
        
    • Click on Save to apply the settings.
        
    • Click on Save to apply the settings.
    
    •  Step-by-Step Guide to Create a SonarQube Token
    
    1. Login to SonarQube:
Open your web browser and navigate to your SonarQube
instance (e.g., http://your-sonarqube-server).Log in with your SonarQube credentials. You need to have
sufficient permissions (typically an administrator or project-
level admin) to create a token.
2. Access Your User Account Settings:
After logging in, click on your user profile avatar or your
username in the top-right corner of the SonarQube dashboard.
From the dropdown menu, select My Account
3. Navigate to Security:
In the My Account section, click on the Security tab on the left sidebar.

4. Generate a New Token:
Under the Generate Tokens section, you will see an option to
create a new token.
• Provide a name for your token (e.g., Jenkins
Integration Token). This name is just a label for you to
recognize the token later.
• Click the Generate button.
5. Copy the Token:
Once the token is generated, it will be displayed on the screen.
Copy the token immediately as it will only be shown once.
Store this token securely, as you’ll need it to configure the
SonarQube integration with Jenkins
6. Use the Token in Jenkins:
Go to your Jenkins dashboard.

Navigate to Manage Jenkins > Manage Credentials.
Add a new Secret text credential where the secret is the
SonarQube token you just generated. Assign an ID (e.g.,
sonar_token) that you can reference in your Jenkins
pipeline.

![image](https://github.com/user-attachments/assets/6737989f-6ba3-4263-9f80-2102eb6acee0)

Step 2: Configure Jenkins Pipeline for SonarQube Analysis
 use above Jenkinsfile 

Step 4: Verifying Integration
Check SonarQube Dashboard:

![image](https://github.com/user-attachments/assets/d20fdeb7-ec61-45c7-ae6c-aebda70d51f5)
