pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Reshma-0654/reshmashaik.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mywebsite .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name mycontainer mywebsite'
            }
        }

    }
}
