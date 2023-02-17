pipeline {
    agent any 
    stages {
        stage('Build') { '
            steps {
                sh 'g++ working.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh './a.out'
                build : 'PES1UG21CS803'
            }
        }
        stage('Deploy') { 
            steps {
                //sh './output'
                error 'Pipeline Failed' 
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
