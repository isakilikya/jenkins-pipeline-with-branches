pipeline {
    agent any
    
    environment {
        VERSION = 'v0.5'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Build'
                echo '$env.BUILD_ID'
                echo '$BUILD_ID'
                echo '$BRANCH_NAME'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                echo '$BRANCH_NAME'
            }
        }
        stage('Develop') {
            when {
                branch 'develop'
            }
            steps {
                echo 'Develop'
                echo '$BRANCH_NAME'
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploy'
                echo '$BRANCH_NAME'
            }
        }
    }
}
