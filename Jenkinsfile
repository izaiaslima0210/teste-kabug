pipeline {
    agent {
        docker {
            image 'izaiaslima/rubywd'

        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building or resolve depedencies'
                sh 'rm -f Gemfile.lock'
                sh 'bundle install'
            }
        }
        stage('Test') {
            steps{
                echo 'Execute teste regression'
                sh 'bundle exec cucumber -p ci'
            }
        }
        stage('UAT'){
            steps{
                echo 'Wait for User Acceptance '
                input(message: 'Go to Production?', ok: 'Yes')
            }
        }
        stage('prod'){
            steps{
                echo 'webApp ready :)'
            }
        }
    }
}
