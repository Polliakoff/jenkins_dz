pipeline {
    agent any

    stages {
        stage('compose') {
            options {
              timeout(time: 10, unit: 'SECONDS')
            }
            steps {
                echo '=========================RUN DOCKER COMPOSE========================='
                sh 'docker-compose up -d'
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
