pipeline {
    agent any
    tools {
        maven 'maven3'
           }
    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/opusheen/demo3.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn package -f' 
            }
        }   
        post {
            success {
            archiveArtifacts(artifacts: '**/target/*.war', allowEmptyArchive: true)
             }
        }
    }
}
