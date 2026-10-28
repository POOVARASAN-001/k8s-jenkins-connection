
pipeline {
    agent any

    environment {
        KUBECTL = 'D:\\DockerApp\\resources\\bin\\kubectl.exe'
        KUBECONFIG = 'C:\\Users\\C:\Users\POOVARASAN\.kube\config\\.kube\\config'
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
