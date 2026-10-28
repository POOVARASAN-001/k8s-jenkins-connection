
pipeline {
    agent any

    stages {
        stage('Check kubectl') {
            steps {
                bat 'kubectl version --client'
            }
        }

        stage('Verify Kubernetes Connection') {
            steps {
                bat 'kubectl config current-context'
                bat 'kubectl cluster-info'
                bat 'kubectl get nodes'
                bat 'kubectl get pods -A'
            }
        }
    }
}
