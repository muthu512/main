pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/muthu512/main.git'
            }
        }
        stage('Build') {
            steps {
                sh './mvnw clean package'
            }
        }
        stage('Run Application') {
            steps {
                sh 'java -jar target/your-app-name.jar'
            }
        }
    }
}

