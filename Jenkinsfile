pipeline {
    agent { docker { image 'golang' } }
    stages {
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh 'go version'
            }
        }
    }
}
