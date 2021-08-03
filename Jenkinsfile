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
			when {
				expression {
					currentBuild.result == null || currentBuild.result == 'SUCCESS'
				}
			}
			steps {
				echo 'this is deploy'
			}
		}
	}
	post {
		success {
			echo 'successfully build'
		}
		failure {
			echo 'Failed'
			mail to gadupudilk@gmail.com, subject: 'java failed'
			
		}
	}
}
		

