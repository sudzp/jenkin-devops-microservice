//DECLARATIVE PIPELINE
pipeline {
//	agent any
	agent { docker { image 'maven:3.6.3'} }

	stages {
		stage("Build"){
			steps{
				echo "Build" 
			}
		}
		stage("Test"){
			steps{
				echo "Test" 
			}
		}
		stage("Integraton Test"){
			steps{
				echo "Integraton Test" 
			}
		}
	}

	post{
		always{
			echo "I am awesome, I run always"
		}
		success{
			echo "I run when I am passed"
		}
		failure{
			echo "I run when I am failed"
		}
	}
	
}
