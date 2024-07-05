pipeline {
    agent any 
    stages {
        stage ('code checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Tejaswi53/multibranchtask1.git']])
            }
        }
        stage('image build') {
            steps {
                sh 'docker build -t apache2 .'
                
            }
        }
        stage ('user acceptance test') {
            steps {
                sh 'docker run -d --name cntr2 -p 8082:80 apache2' 
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