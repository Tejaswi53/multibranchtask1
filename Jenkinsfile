pipeline {
    agent any 
    stages {
        stage ('code checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Tejaswi53/multibranchtask1.git']])
            }
            
        }
        stage ('unit testing') {
            steps {
                sh '''
                    echo "unit testing"
                '''
            }
        }
        stage ('code analysis') {
            steps {
                sh '''
                    echo "code analysis"
                '''
            }
        }
        stage ('deployement') {
            when {
                branch 'develop'
            }
            steps {
                sh '''
                    echo "deployement"
                '''
            }
        }
    }
}