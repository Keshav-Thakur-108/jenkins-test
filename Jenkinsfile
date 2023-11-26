pipeline {
    agent {
        label 'agent1'
    }

    options {
        skipDefaultCheckout()
    }

    stages {
        stage('Build') {
            steps {
                sh 'cat normal.txt'
            }
        }
    }
}