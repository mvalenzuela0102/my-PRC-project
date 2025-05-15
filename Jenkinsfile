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
                bat 'echo Laboratorio 4'
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
