
pipeline{
	agent {label 'master'}
	tools{ maven 'M3'}
	stages{
		stage('Checkout'){
			steps{
				git 'https://github.com/AnjuMeleth/spring-petclinic.git'
			}
		}
		stage(' Build') {
			steps {
				sh 'mvn clean compile'
			}
		}
		stage(' Test') {
			steps {
				sh 'mvn test'
			}
		}
                stage(' Package') {
			steps {
				sh 'mvn package'
			}
		}	
					
	}
}
