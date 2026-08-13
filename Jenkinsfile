pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'mvnw.cmd clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvnw.cmd test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvnw.cmd package -DskipTests'
            }
        }
    }

    post {
        success {
            echo 'BUILD, TEST AND PACKAGE SUCCESSFUL!'
        }

        failure {
            echo 'PIPELINE FAILED!'
        }
    }
}