pipeline {

    agent none
    
    stages {
        stage ('test') {
            agent {
                docker {image 'maven:3.8.1-adoptopenjdk-11'}
            }
            steps {
                sh '''
                mvn
                env
                '''
            }
        }
         
        stage ('build') {
            agent {
                docker {image 'node:16-alpine'}
            }
            steps {
                sh '''
                node --version
                env
                '''
            }
        }
        
    }
    
}
