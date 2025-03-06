pipeline {
    agent any 
    stages {
        stage('DockeBuildPush') {
            steps {
                sh "docker pull nginx"
                echo "*************************** Printing the images *********************************"
                sh "docker images"
            }
        }
    }
}
