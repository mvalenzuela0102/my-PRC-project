pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Built') {
            steps {
                bat 'python --version'
            }
        }
    }
}
