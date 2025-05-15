pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build') {
            steps {
                bat 'docker build -t my-python-app .'
            }
        }
        stage('Deploy') {
            steps {
                // Arranca el contenedor exponiendo el puerto 80 interno en el 8001 local
                bat 'docker run -d -p 8001:80 my-python-app'
            }
        }
    }

    post {
        success {
            echo 'Build completado exitosamente'
        }
        failure {
            echo 'Build fallido'
        }
    }
}
