pipeline{
	
	environment{
		registry = 'pallavideshmanedockerid/dockerizejenkins'
		registryCredential = 'dockerid'
		dockerImage = ''
	}
	
	agent any
	stages{
		stage('cloning git') {
			steps{
				git 'https://github.com/pd70193/DockerizeJenkins.git'
			}
		}
		
	  stage('Building image'){
	  	steps{
	  		script{
	  			dockerImage = docker.build registry + ":$BUILD_NUMBER"
	  		}  	
	  	}	  
	  }	
	  
	  stage('Deploy Image'){
	  	steps{
	  		script{
	  			docker.withRegistry('',registryCredential){
	  				dockerImage.push()
	  			}
	  		}
	  	}
	  }
	}
}
