pipeline {
    agent any 
    stages {
        stage('Build') { '
            steps {
                sh 'g++ -o output PES1UG21CS803.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh 'cat PES1UG21CS803.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                //sh './output'
                error'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
