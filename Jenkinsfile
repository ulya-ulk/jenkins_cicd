pipeline {
    agent {
        label 'new_pipeline'
    }
    

    	environment {
            envString = 'true'
		
	}

    post {
        always {
            bat 'echo hello'
        }

        failure {
            bat 'echo failure'
        }

        success {
            bat 'echo success'
        }

    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ulya-ulk/jenkins_cicd.git'
            }
        }
        
        stage('Build test base') {
            steps {
                bat "echo Build test base"
            }
        }
                
    }
    

}