//DECLARATIVE PIPELINE
pipeline {

	//agent any

	 agent {
         docker { image 'node:7-alpine' }
     }

	stages {
		stage("Build"){
			steps{
				echo "Build" 
				echo "$PATH"
				echo "Build Number - $env.BUILD_NUMBER"
				echo "Build Id - $env.BUILD_ID"
				echo "Job Name - $env.JOB_NAME"
				echo "Build Tag - $env.BUILD_TAG"
				echo "Build URL - $env.BUILD_URL"
				
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
