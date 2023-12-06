pipeline {
    agent any

    stages {

        stage('Build') {
            when {
                tag '2.0'
            }

            steps {
                echo 'Hello world'
            }
        }

        stage('Build Changelog') {
            when {
                changelog '.*some_text.*'
            }

            steps {
                echo 'Build Changelog worked just fine'
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