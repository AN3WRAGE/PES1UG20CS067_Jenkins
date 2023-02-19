pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o output 1.cpp'
                echo 'Build stage successful'
            }
        }
        stage('Test') { 
            steps {
                sh 'cat 1.cpp'
                echo 'Test stage successful'
            }
        }
        stage('Deploy') { 
            steps {
                error 'Pipeline Failed' 
//                 sh './output'
                echo 'Deploy stage successful'
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
