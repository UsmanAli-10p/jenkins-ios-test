pipeline {
    agent any

    stages {
        stage('Install Gems') {
            steps {
                dir ('MasterDetailApp') { 
                    sh 'sudo bundle install'
                }
            }
        }
        stage('Generate IPA for master') {
        	when { branch 'master' }
            steps {
                dir ('MasterDetailApp') { 
                    sh 'bundle exec fastlane prod'
                }
            }
        }
        stage('Generate IPA for development') {
        	when { branch 'development' }
            steps {
                dir ('MasterDetailApp') { 
                    sh 'bundle exec fastlane developerRelease'
                }
            }
        }
        stage('Generate IPA for qa') {
        	when { branch 'qa' }
            steps {
                dir ('MasterDetailApp') { 
                    sh 'bundle exec fastlane qaRelease'
                }
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'MasterDetailApp/output/**', fingerprint: true
        }
    }
}