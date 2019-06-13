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
                ./gradlew clean test jar
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
            archiveArtifacts 'build/libs/*'
            }
        }
    }
    
}
