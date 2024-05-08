pipeline {
agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Patuuuska/java-todo-jenkins'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage"
                sh "docker build -t obraz -f ./building/Dockerfile ."
            }
        }

        stage('Test') {
            steps {
                echo "Test stage"
                 sh "docker build -t obraz -f ./test/Dockerfile ."
            }
        }

    }
    post{
        success {
            echo 'Success'
        }
        failure {
            echo 'Failed'
        }
    }

}

