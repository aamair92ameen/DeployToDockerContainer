pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the application..."'
                sh 'cp index.html build/'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying the application..."'
                sh 'docker run -d -p 80:80 -v $(pwd)/build:/usr/share/nginx/html nginx'
            }
        }
    }
}
