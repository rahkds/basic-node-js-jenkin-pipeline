pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true' 
    }
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