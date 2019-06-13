pipeline {
    agent any
    
    stages {
        stage('greetings') {
            steps{
                echo 'Holla Mundos!'
            }
        }
        stage ('Preperation'){
            steps{
                echo 'Preperation'
                sh './gradlew clean test jar'
            }
        }
        stage ('Build'){
            steps{
                echo 'Build'
            }
        }
        stage ('Result'){
            steps{
                echo 'Result'
                junit '**/build/test-results/test/TEST-*.xml'
                archive 'build/libs'
            }
        }
    }
    
}
