pipeline {
    agent {label 'slave-1'}
    
        tools {
            maven 'maven3'
           
        }

    stages {
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
