pipeline {
    agent any
    stages {
        stage("Install dependencies") {
            sh "npm install"
        }
        stage("Run Test") {
            sh "npm run test"
        }   
        
        stage("Deploy and run server") {
            sh "npm run start"
        }             

    }
}