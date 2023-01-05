pipeline {
    agent any 
    
    tools {
        maven 'Maven3'
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/dvmane100/XperitRepo2023.git']])
            }
        }      
        stage ('Build') {
            steps {
                sh 'mvn clean install'           
            }
        }   
    }
}
