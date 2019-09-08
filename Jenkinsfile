
pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
               checkout scm                 
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('deployment package') {
            steps {
             xldCreatePackage artifactsPath: '/target/', darPath: 'petclinic-test.dar', manifestPath: 'deployit-manifest.xml'   
            }
        }
                             
    }
}
