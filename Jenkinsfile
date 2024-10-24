pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/muthu512/main.git' // Replace with your repository URL
            }
        }

        stage('Build') {
            steps {
                sh './mvnw clean package'
            }
        }

        stage('Run Application') {
            steps {
                sh 'java -jar target/online-1-0.0.1-SNAPSHOT.jar' // Adjust path if necessary
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build or deployment failed.'
        }
    }
}

