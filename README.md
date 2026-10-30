# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC  for integrating postman tests with github actions. The tests are written in postman and they are executed on the VM with the help of
newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The projects runs on a scheduled time 
with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : 
 https://hinduja-sundararajan.github.io/SamplePostmanProject/
 
 The latest report is mailed to the team members using GMAIL SMTP.

 ## About Me ##
 Hi My Name is Hinduja. I have 6 years of experience in Automation Testing and DevOps. My Skillset Includes UI Automation with Selenium Webdriver and for API Testing I use 
 Rest Assured and Postman. 

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets
   
 ## Tech Stack ##
 1. Postman
 2. Nodejs 22v
 3. Newman
 4. Newman-Reporter-Htmlextra
 5. Github Actions
 6. Gmail SMTP
 7. Github pages
 8. CSV for Data Driven Testing
 9. AWS-EC2 instance for self hosted github runner.

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/Hinduja-Sundararajan/SamplePostmanProject/blob/static-content/newman-report.png)

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link :  https://hinduja-sundararajan.github.io/SamplePostmanProject/

# How to run the Project? #
To run the project on your local system:
1. Clone the project on your local system : https://github.com/Hinduja-Sundararajan/SamplePostmanProject.git
2. Install Nodejs and NPM from : https://www.npmjs.com/
3. Install Newman :``` npm install -g newman ```
4. Install Newman-reporter-htmlextra :``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman command :```
           newman run 'InWarrantyFlow.postman_collection_main.json' \
           --env-var="Domainname=http://64.227.160.186:9000/v1" \
           -r cli,htmlextra \
           --reporter-htmlextra-export ./newman/index.html   ```

## Project Structure ##
```
SamplePostmanProject
└─ inwarranty flow
   ├─ InWarrantyFlow.postman_collection.json #collection file which uses user-defined testdata
   ├─ InWarrantyFlow.postman_collection_main.json #collection file which uses random testdata
   └─ testdata.csv #test data file

```

