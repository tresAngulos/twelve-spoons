pipeline {
    agent { docker { image 'golang' } }
    triggers { githubPush() }
    stages {
        stage('build') {
            steps {
                sh 'go version'
            }
        }
    }
}
