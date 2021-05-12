pipeline {
    agent { docker { image 'golang' } }
    stages {
        triggers {
            githubPush()
        }
        stage('build') {
            steps {
                sh 'go version'
            }
        }
    }
}
