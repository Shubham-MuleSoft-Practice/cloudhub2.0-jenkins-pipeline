pipeline
{
	agent any
	stages{
		stage('Build Application') {
			steps {
			   bat 'mvn clean install'
		   }
	    }
		stage('Test') {
			steps {
			   bat ‘mvn test’
		   }
	    }
		stage('Deploy CloudHub 2.0) {
			steps {
			   bat 'mvn clean deploy -DmuleDeploy -Duser=Shubh_123 -Dpass=Shubh@123'
			}
		}
    }
	
}