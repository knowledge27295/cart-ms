pipeline {
    agent any 
    stages {
        stage('DockeBuildPush') {
            steps {
                sh "docker pull nginx"
                echo "*************************** Printing the images *********************************"
                sh "docker images"
                sh "docker tag nginx devopswithcloudhub/nginxdevops:b6"
                sh "docker push devopswithcloudhub/nginxdevops:b6"
            }
        }
    }
}
