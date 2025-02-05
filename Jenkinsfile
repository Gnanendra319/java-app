pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t my-java-app .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -p 8080:8080 my-java-app'
            }
        }
    }
}
