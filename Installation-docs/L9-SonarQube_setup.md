## SonarQube Configuration 

1. Setup SonarQube server.
        `OR` Create Sonar cloud account on https://sonarcloud.io
3. Generate an Authentication token on SonarQube
    Account --> my account --> Security --> Generate Tokens 

4. On Jenkins create credentials 
   Manage Jenkins --> manage credentials --> system --> Global credentials --> add credentials
 - Credentials type: `Secret text`
 - ID: `sonarqube-key`

5. Install SonarQube plugin
    Manage Jenkins --> Available plugins 
    Search for `sonarqube scanner`

6. Configure sonarqube server 
   Manage Jenkins --> Configure System --> sonarqube server 
   Add Sonarqube server 
   - Name: `sonar-server`
   - Server URL: `<private_ip>`
           `OR` `https://sonarcloud.io/`
   - Server authentication token: `sonarqube-key`

7. Configure sonarqube scanner 
   Manage Jenkins --> Global Tool configuration --> Sonarqube scanner 
   Add sonarqube scanner 
   - Sonarqube scanner: `sonar-scanner`
