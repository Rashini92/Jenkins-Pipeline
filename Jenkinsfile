pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                echo "Build the code using a build automation tool 'Maven' to compile and package the code."
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "Run unit tests to ensure the expected code functionalities"
                echo "Run integration tests to ensure the different components of the application work together as expected"
                echo "use the 'Selenium' test austomation tool for the above tests"
            }
        }
        stage('Code Analysis'){
            steps{
                echo "integrate the tool 'SonarQube' to analyse the code and ensure it meets industry standards using "
            }
        }
        stage('Security Scan'){
            steps{
                echo "perform a security scan on the code using 'Codiga' tool to identify any vulnerabilities"
            }
            post{
                success{
                    mail to:"rashinijayanga@gmail.com",
                    subject:"Security Scan stage email",
                    body:"Security Scan was successful"
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "deploy the application to a staging server- AWS EC2 instance"
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo "run integration tests on the staging environment to ensure the application functions as expected in a production-like environment."
            }
            post{
                success{
                    mail to:"rashinijayanga@gmail.com",
                    subject:"Integration Test stage email",
                    body:"Integration Tests were successful"
                }
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deploy the code to the production server-AWS EC2 instance"
            }
        }
    } 
}
