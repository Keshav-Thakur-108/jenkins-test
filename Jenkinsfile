pipeline {
    agent {
        label 'agent1'
    }

    stages {
        stage('Master') {
            when {
                branch: 'master'
            }
            steps {
                sh 'cat normal.txt'
            }
        }

        stage('Dev') {
            options {
                skipDefaultCheckout()
            }

            steps {
                echo "Hello World!"
            }
        }
    }
}