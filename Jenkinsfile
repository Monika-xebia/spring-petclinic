
pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
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
