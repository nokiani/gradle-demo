pipeline {
    agent any
    
    
    tools {
        gradle 'gradle691'
    }
    
    stages {
        
        stage("Test") {
            steps {
            echo 'executing gradle...'
            sh 'pwd'
            sh 'ls -la'
            sh './gradlew -v'
            }
        }
        
        stage ('Build Artifact') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh "./gradlew clean build"
            }
        }
        
    }
}
