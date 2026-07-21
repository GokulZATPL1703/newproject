pipeline {
    agent any
    stages {
        stage('Checkout'){
            steps {
                echo 'Getting source code....'
                checkout scm
            }
        }
        stage('compile'){
            steps {
                echo 'Compiling Java Program...'
                bat 'javac Hello.java'
            }
        }
        stage('Run'){
            steps {
                echo 'Running Java Program...'
                bat 'java Hello'
            }
        }

    }
    post {
        always {
            echo 'Pipeline Completed'
        }

        success {
            echo 'Build Successful'
        }

        failure {
            echo "Build Failed"
        }
    }
}