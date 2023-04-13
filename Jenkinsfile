pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Building the application..."'
                bat 'cp index.html build/'
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo "Deploying the application..."'
                bat 'docker run -d -p 80:80 -v $(pwd)/build:/usr/share/nginx/html nginx'
            }
        }
    }
}
