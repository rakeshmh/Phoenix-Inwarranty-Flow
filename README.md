#Postman API automation integraiton with github Action#

This repository is a demonstration of POC for integratin postman tests with github acitons. The Test are written in postman and they are executed on the VW with the help of newman and newman-reporter-htmlextra. 
Github action will trigger the project exectuion on every push to the main branch. You can also execute the project manually using work_flow dispatch. The project runs on scheduled time with the help on cron job.

The project report is archived and kept in the artifact section for the team to downalod. Alogn with that they can directly view the report from the github page : https://rakeshmh.github.io/Phoenix-Inwarranty-Flow/

The latest report is mailed to the team members using GMAIL SMTP

##Tech Stack##
1. Postman
2. Node js
3. Newman
4. Newman-report-extra
5. Gmail SMTP
6. Github actions
7. Github pages
8. CSV for data driven testing
9. AWS-EC2

##Github Pages##
You can direclty view the latest test report on the github page link : https://rakeshmh.github.io/Phoenix-Inwarranty-Flow/

##How to run the project##I
You can run the project from your local system for that:
1. Clone the project on local system : https://rakeshmh.github.io/Phoenix-Inwarranty-Flow/
2. Install Node JS and npm from http://nodejs.org/en
3. Install newman using npm install -g newman
4. Install newman-reporter-htmlextra npm install -g newman-reporter-htmlextra
5. Run the Newman Command:
                newman run "Inwarranty - Flow Collection.postman_collection.json"\
                -e QA.postman_environment.json \
                -d testdata.csv \
                -r cli,htmlextra
                --reporter-htmmlextra-export ./newman/index.html

##HTML Report##
The reporte will be created in newman folder
![PostmanReport](https://github.com/rakeshmh/Phoenix-Inwarranty-Flow/blob/static-content/NewmanReport.png)
