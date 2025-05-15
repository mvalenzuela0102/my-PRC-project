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
                bat 'docker build -t my-python-app .'
            }
        }
    }
    post {
        success {
            echo "Build completado exitosamente"
            }
         failure {
              echo "build fallido"
            }
        }
}
