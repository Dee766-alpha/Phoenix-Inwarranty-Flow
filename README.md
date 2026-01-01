# Postman API Automation Integration with GithubAction #

This repository is a demonstration for POC for integrating Postman tests with github actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch.You can also execute the project manually using worflow_dispatch.The projects runs on a scheduled time with the help of the cron job.

The HTML report is achieved and kept in the artifact section for the team to download it.Along with that they can view the report directly from the github page :https://dee766-alpha.github.io/Phoenix-Inwarranty-Flow/

The latest report is mailed to the team members using GMAIL SMTP.
 ## About Me ##
 Hi My name is Deepali having 5 yr of experience in testing .My skillset includes UI Automation with selenium Webdriver and Devops.
## Testing Coverage ##
1.Happy Flow Testing
2.Negative testing and Edge case Testing
3.Token testing
4. data driven testing with CSV
5.Schema Validation
6.Secrets management with Github secrets


## Tech Stack ##
1.Postman
2.Nodejs 22v
3.Newman
4.Newman-Reporter-Htmlextra
5.Github Actions
6.Gmail SMTP
7.Github Pages
8.CSV for Data Driven Testing
9.AWS-EC@ instance for self hosted github runner

## Github Pages ##

You can directly view the latest test report of the postman test at the Github Page Link :https://dee766-alpha.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the newman folder 
![Postman Report](https://github.com/Dee766-alpha/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##

```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json #Collection File
├─ QA.postman_environment.json #Environment File
└─ testData.csv #Testdata File

```

## How to run the Project? ##
You can run the project on your local system for that:
1.Clone the project on local system : https://github.com/Dee766-alpha/Phoenix-Inwarranty-Flow.git
2.Install Node js and NPM from https://nodejs.org/en
3.Install Newman using  ```npm install -g newman```
4.Install Newman-reporter-htmlextra ``` npm install -g newman-reporter-htmlextra ```
5.Run the Newman command:
```
                newman run 'Inwarranty-flow Collection.postman_collection.json' \
               -e QA.postman_environment.json \
               -d testdata.csv \
               -r cli,htmlextra \
               --reprter-htmlextra-export ./newman/index.html
```





