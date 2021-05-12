pipeline {
    agent { docker { image 'golang' } }
    stages {
        stage('Checkout SCM') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: 'master']],
                    userRemoteConfigs: [[
                        url: 'git@github.com:wshihadeh/rabbitmq_client.git',
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
