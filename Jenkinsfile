pipeline {
    agent any
    stages {
        stage('Install Docker ') {
            steps {
                script {
                    // Installation of docker for CentOS
                    sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                    sh 'chmod +x get-docker.sh'
                    sh 'sudo ./get-docker.sh '
                    sh 'sudo systemctl start docker'
                    sh 'sudo systemctl enable docker'
                }
            }
        }
        stage('Test the docker') {
            steps {
                script {
                    // Version check
                    sh 'sudo docker version'
                    //Run a single docker container
                    sh 'sudo docker pull docker/whalesay'
                    sh 'sudo docker run docker/whalesay cowsay boo'
                    // Szóellenőrzés
              
                }
            }
        }

    }
}
