pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/sunnyajay293/devops-project-2.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5001:5000 devops-app'
            }
        }
    }
}
