//DECLARATIVE PIPELINE
pipeline {

	agent any

	//  agent {
    //      docker { image 'node:7-alpine' }
    //  }

	environment{
		dockerHome = tool "myDocker"
		mavenHome = tool "myMaven"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage("Checkout"){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Build" 
				echo "$PATH"
				echo "Build Number - $env.BUILD_NUMBER"
				echo "Build Id - $env.BUILD_ID"
				echo "Job Name - $env.JOB_NAME"
				echo "Build Tag - $env.BUILD_TAG"
				echo "Build URL - $env.BUILD_URL"
				
			}
		}
		stage("Compile"){
			steps{
				sh "mvn clean compile"
			}
		}
		stage("Test"){
			steps{
				sh "mvn test"
			}
		}
		stage("Integraton Test"){
			steps{
				sh "mvn failsafe:integration-test failsafe:verify"
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
