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
    }
    post {
        always {
            archiveArtifacts artifacts: 'MasterDetailApp/output/**', fingerprint: true
        }
    }
}