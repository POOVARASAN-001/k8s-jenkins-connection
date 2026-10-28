
pipeline {
    agent any

    environment {
        KUBECTL = 'D:\\DockerApp\\resources\\bin\\kubectl.exe'
        KUBECONFIG = 'C:\\Users\\YOUR_WINDOWS_USERNAME\\.kube\\config'
    }

    stages {
        stage('Check kubectl') {
            steps {
                bat '"%KUBECTL%" version --client'
            }
        }

        stage('Verify Kubernetes Connection') {
            steps {
                bat '"%KUBECTL%" config current-context'
                bat '"%KUBECTL%" cluster-info'
                bat '"%KUBECTL%" get nodes'
                bat '"%KUBECTL%" get pods -A'
            }
        }
    }
}
