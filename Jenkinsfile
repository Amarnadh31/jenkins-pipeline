pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        disableConcurrentBuilds()
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
    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success {
            echo 'pipeline is successful'
        }
    }
}