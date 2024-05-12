```pipeline {
    agent any
    
    stages {
        stage('Git Clone') {
            steps {
                git 'https://github.com/yashwanthnatha/Devops.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh 'javac -d target/classes main/*/.java'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}