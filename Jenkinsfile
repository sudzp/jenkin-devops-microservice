//DECLARATIVE PIPELINE
pipeline {
//	agent any
	agent {
  		label 'nodeDocker'
	}

	// agent {
    //     docker { image 'node:7-alpine' }
    // }

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
