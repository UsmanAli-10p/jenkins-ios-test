pipeline {
    agent any

    stages {
        stage('Install Gems') {
            steps {
                sh 'cd MasterDetailApp'
                sh 'bundle install'
            }
        }
        stage('Install Pods') {
            steps {
                sh 'bundle exec pod install'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}