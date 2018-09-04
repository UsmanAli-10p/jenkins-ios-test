pipeline {
    agent any

    stages {
        stage('Install Gems') {
            dir ('MasterDetailApp') {
                steps {
                    sh 
                    sh 'bundle install'
                }
            }
        }
        stage('Install Pods') {
            dir ('MasterDetailApp') {
                steps {
                    sh 'bundle exec pod install'
                }
            }
        }
        stage('Build') {
            dir ('MasterDetailApp') {
                steps {
                    echo 'Building..'
                }
            }
        }
        stage('Test') {
            dir ('MasterDetailApp') {
                steps {
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            dir ('MasterDetailApp') {
                steps {
                    echo 'Deploying....'
                }
            }
        }
    }
}