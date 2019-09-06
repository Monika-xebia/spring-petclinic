
pipeline {
    agent any
    stages {
        stage ('checkout') {
            steps {
               checkout scm                 
            }
        }
        stage('build') {
            steps {
                sh 'mvn --version'
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
        stage('deploy') {
            steps {
              sh 'mvn deploy'
            }
            
        }
    }
}
