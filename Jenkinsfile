pipeline {
    agent any
    parameters {
        string(name: 'GREETING', defaultValue: 'Hello', description: 'The greeting message is here!')
        choice(name: 'BRANCH', choices: ['master','dev','main'], description: 'Branch to build')
    }
    stages {
         stage('Example') {
            steps {
                echo "${params.GREETING}, we are building the ${params.BRANCH} branch."
            }
        }
        stage('Test') {
            steps {
                echo 'Testowanie aplikacji...'
            }
        }
        }
    }

