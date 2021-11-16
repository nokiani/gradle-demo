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
                sh "./gradlew build"
            }
        }
        
        stage ('Docker Build') {
            agent {
                dockerfile {
                    filename 'Dockerfile.only-package'
                }
            }
            steps {
                echo 'Docker building...'
            }
        
    }
}
