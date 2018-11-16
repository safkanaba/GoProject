pipeline {
    agent { docker { image 'golang' } }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh 'go version'
                sh 'printenv'
            }
        }
	    stage('test') {
	        steps {
	            timeout(time: 5, unit: 'MINUTES') {
                    retry(5) {
                        sh 'echo "deneme deneme"'
                    }
                }
            }		
        }
    }
    post {
	    always {
	        echo 'always'
	    }
        success {
	        echo 'dimi'
	    }
    }
}
