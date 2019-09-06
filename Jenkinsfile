
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
        stage('package') {
            steps {
                xldCreatePackage artifactsPath: '/var/lib/jenkins/workspace/xld-petclinic/target/', darPath: 'output.dar', manifestPath: 'deployit-manifest.xml'
            }
        }
                     
    }
}
