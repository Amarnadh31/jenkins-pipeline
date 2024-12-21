pipeline {
    agent {
        label 'AGENT-2'
    }
    options {
        disableConcurrentBuilds()
    }
     parameters {
        string(name: 'AMAR', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
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