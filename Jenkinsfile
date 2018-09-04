pipeline {
    agent any

    stages {
        stage('Install Gems') {
            steps {
                dir ('MasterDetailApp') { 
                    sh 'bundle install'
                }
            }
        }
        stage('Generate IPA') {
            steps {
                dir ('MasterDetailApp') { 
                    sh 'bundle exec fastlane qaRelease'
                }
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