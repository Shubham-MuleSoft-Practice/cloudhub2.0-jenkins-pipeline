pipeline
{
	agent any
	stages{
		stage(‘Build Application’) {
			steps {
			   bat ‘mvn clean install’
		   }
	    }
		stage('Test') {
			steps {
			   bat ‘mvn test’
		   }
	    }
		stage(‘Deploy CloudHub’) {
			steps {
			   bat ‘mvn clean deploy -DmuleDeploy -Duser=Shubh_123 -Dpass=Shubh@123’
			}
		}
    }
	
}