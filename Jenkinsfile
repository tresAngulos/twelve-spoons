pipeline {
    agent { docker { image 'golang' } }
    stages {
        stage('Checkout SCM') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: 'main']],
                    userRemoteConfigs: [[
                        url: 'git@github.com/tresAngulos/twelve-spoons.git',
                        credentialsId: '',
                    ]]
                ])
            }
        }
        stage('build') {
            steps {
                sh 'go version'
            }
        }
    }
}
