pipeline {
    agent any 
    stages {
        stage('Build') { '
            steps {
                sh 'g++ PES1UG21CS803.cpp'
                build : 'PES1UG21CS803-1'
            }
        }
        stage('Test') { 
            steps {
                s './a.out'
            }
        }
        stage('Deploy') { 
            steps {
                error'Pipeline Deployed' 
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
