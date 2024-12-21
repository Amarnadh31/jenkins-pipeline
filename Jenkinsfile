pipeline {
    agent {
        label 'AGENT-1'
    } 
    stages {
        stage('Build') { 
            steps {
                script{
                    sh "echo hello world, this is build stage"
                }
            }
        }
        stage('Test') { 
            steps {
                script{
                    sh "echo hello world, this is Test stage"
                } 
            }
        }
        stage('Deploy') { 
            steps {
                script{
                    sh "echo hello world, this is Deploy stage"
                }
            }
        }
    }
}