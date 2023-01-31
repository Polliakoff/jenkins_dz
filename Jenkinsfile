pipeline {
    agent any

    stages {
        stage('compose') {
            steps {
                echo '=========================RUN DOCKER COMPOSE========================='
                sh 'docker-compose up -d'
                echo '=========================CHECK OUTPUT========================='
                sh 'curl localhost:8090'
            }
        }
    }
}
