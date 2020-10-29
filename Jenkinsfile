pipeline{
	
	environment{
		registry = 'pallavideshmanedockerid/dockerizejenkins'
		registryCredential = 'mydockercred'
		dockerImage = ''
	}
	
	agent any
	stages{
		
		stage('test'){
			steps{
			echo "test stage"
			}
		}
		stage('cloning git') {
			steps{
				git 'https://github.com/pd70193/DockerizeJenkins.git'
			}
		}
		
	}
}
