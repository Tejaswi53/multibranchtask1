pipeline{
    agent any
    stages {
        stage('master branch') {
            when {
                branch 'main'
            }
            steps {
                sh '''
                    echo "Build artifacts from master branch"
        
                '''    
            }
        }
        stage('feature1 branch') {
            when {
                branch 'feature1'
            }
            steps {
                sh '''
                    echo "build artifacts from the feature1 branch"
                '''    
            }
        }
    }
}