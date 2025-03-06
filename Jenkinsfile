pipeline {
    agent any
    environment {
        DOCKER_CREDS = credentials('dockerhub_creds')
        DOCKER_REPO = "devopswithcloudhub/nginxdevops"
    } 
    stages {
        stage('DockeBuildPush') {
            steps {
                sh "docker pull nginx"
                echo "*************************** Printing the images *********************************"
                sh "docker images"
                sh "docker tag nginx ${DOCKER_REPO}:b6"
                echo "************************ Docker login ********************************"
                sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
                sh "docker push ${DOCKER_REPO}:b6"
            }
        }
    }
}
