pipeline {
    agent any
    parameters {
        string(name: 'GREETING', defaultValue: 'Hello', description: 'The greeting message is here!')
        choice(name: 'BRANCH', choices: ['master','dev'], description: 'Branch to build')
        booleanParam(name: 'DEPLOY', defaultValue: true, description: 'Czy uruchomić etap wdrożenia?')
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
         stage('Deploy') {
            when {
                expression { params.DEPLOY }
            }
            steps {
                echo 'Wdrażanie aplikacji...'
            }
        }
    }
}

