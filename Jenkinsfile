pipeline {
    agent any
    
    stages {
        stage('Preparation') {
            steps{
                echo 'Preparation'
            }
        }
	stage('Build') {
            steps{
                echo 'Build'
		sh './gradle clean test jar'
            }
        }
	stage('Results') {
            steps{
                echo 'Results'
		junit 'build/reports/**/*.xml'
		archive 'build/libs'
            }
        }
    }
}
