pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/yashwanthnatha/Devops.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Build and compilation successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
