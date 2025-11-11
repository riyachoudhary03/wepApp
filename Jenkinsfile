pipeline {
    agent any 
    
        tools {
            maven 'maven3'
           
        }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/riyachoudhary03/wepApp.git'
            }
        }
        stage('compile') {
            steps {
               sh 'mvn compile'
            }
        }
       stage('test') {
            steps {
               sh 'mvn test'
            }
        }
        
        stage('build') {
            steps {
               sh 'mvn package'
            }
        }
    }
}
