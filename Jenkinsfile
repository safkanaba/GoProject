pipeline {
    agent { docker { image 'golang' } }
    stages {
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh 'go version'
            }
        }
	stage(‘test’) {
	   timeout(time: 5, unit: ‘MINUTES’) {
              retry(5) {
                sh ‘echo “deneme deneme”’
              }
           }		
        }
    }
}
