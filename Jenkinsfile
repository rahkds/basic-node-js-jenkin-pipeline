pipeline {
    agent any
    tools {nodejs "nodejs"}
    stages {
        stage("Install dependencies") {
            steps {
                 sh "npm install"
            }
           
        }
        stage("Run Test") {
            steps {
                sh "npm run test"
            }
        }   
        
        stage("Deploy and run server") {
            steps {
                sh "npm run start"
            }
        }             

    }
}