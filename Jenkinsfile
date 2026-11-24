pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Getting source code from GitHub'
                checkout scm
            }
        }

        stage('Compile Java') {
            steps {
                echo 'Compiling Java program'
                sh 'javac MatrixMultiplication.java'
            }
        }

        stage('Run Java Program') {
            steps {
                echo 'Executing Java program'
                sh 'java MatrixMultiplication'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL!'
        }

        failure {
            echo 'BUILD FAILED!'
        }
    }
}
