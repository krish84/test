pipeline {
    agent any
    parameters {
        choice ( choices: ["TEST", "BUILD"],
                name: 'myparam',
                description: '')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when {
                expression { params.myparam == 'TEST' }
            }
            steps {
                echo 'Testing..'
            }
            
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
