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
	   steps {
	      timeout(time: 5, unit: ‘MINUTES’) {
                 retry(5) {
                   sh ‘echo “deneme deneme”’
                 }
              }
           }		
        }
    }
    post {
	always {
	  echo ‘always’
	}
        success {
	  echo ‘dimi’
	}
    }
}
