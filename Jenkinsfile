pipeline {
    agent any

    stages {
        stage('compose') {
            steps {
                echo '=========================RUN DOCKER COMPOSE========================='
                sh 'docker-compose up -d'
                sh 'sleep 5'
            }
        }
        stage('verify'){
            steps {
                echo '=========================CHECK OUTPUT========================='
                echo '==============(may fail if a firewall is enabled)============='
                sh 'curl localhost:8090'
            }
        }
    }
}
