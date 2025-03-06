pipeline {
    agent any 
    stages {
        stage ("DeployToDev") {
            steps {
                echo "Deploying to Dev environment"
            }
        }
        stage ("DeployToProd") {
            steps {
                when {
                    // branch condition
                    expression { BRANCH_NAME ==~ /(production|staging)/}
                }
                echo "Deploying to prod environment "
            }
        }
    }
}
