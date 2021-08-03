pipeline{
	agent any
	
	stages {
		stage ('Compile') {
			steps {
				echo 'this is compilation phase'
				sh 'javac Main.java'
			}
		}
		stage ('Run') {
			steps {
				echo 'this is Run step'
				sh 'java Main'
			}
		}
		stage ('Deploy') {
			stage {
				echo 'this is deploy'
			}
		}
	}
	success {
		echo 'successfully build'
	}
	failure {
		echo 'Failed'
	}
}
		

