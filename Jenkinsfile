
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
                sh 'mvn clean package'
            }
        }
        stage ('create deployment package') {
            steps {
                xldCreatePackage artifactsPath: '/var/lib/jenkins/workspace/xld-petclinic/target/', darPath: 'output.dar', manifestPath: '/var/lib/jenkins/workspace/xld-petclinic/deployit-manifest.xml'
            }
        }
      
    }
}
