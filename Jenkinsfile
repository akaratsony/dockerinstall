pipeline {
    agent any
    stages {
        stage('Install Docker ') {
            steps {
                script {
                    // Installation of docker for CentOS
                    sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                    sh './get-docker.sh --dry-run'
                }
            }
        }
        stage('Test the docker') {
            steps {
                script {
                    // Version check
                    sh 'docker version'
                    //Run a single docker container
                    sh 'docker pull docker/whalesay'
                    sh 'docker run docker/whalesay cowsay boo'
                    // Szóellenőrzés
              
                }
            }
        }

    }
}
