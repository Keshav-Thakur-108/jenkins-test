pipeline {
    agent {
        label 'agent1'
    }

    stages {

        stage('Build') {
            when {
                tag '1.0'
            }

            steps {
                echo 'Hello world'
            }
        }

        stage('Master') {
            when {
                branch 'master'
            }
            steps {
                sh 'cat normal.txt'
            }
        }

        stage('Dev') {
            when {
                branch 'dev'
            }
            options {
                skipDefaultCheckout()
            }

            steps {
                echo "Hello World!"
            }
        }
    }
}