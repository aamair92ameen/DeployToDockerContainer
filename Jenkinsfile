pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Building the application..."'
                bat 'if not exist build (mkdir build)'
                bat 'copy index.html build\\'
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo "Deploying the application..."'
                bat 'docker run -d -p 80:80 -v %cd%/build:/usr/share/nginx/html nginx'
            }
        }
    }
}
