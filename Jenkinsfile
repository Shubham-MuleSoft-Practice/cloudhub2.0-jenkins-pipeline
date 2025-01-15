pipeline
{
	agent any
	stages{
		stage('Build Application') {
			steps {
			   bat 'mvn -U clean install'
		   }
	    }
		  stage('Run MUnit Tests') {
            steps {
                echo '***** Running MUnit test cases *****'
                bat 'mvn clean test'
            }
        }
		stage('Deploy CloudHub 2.0') {
			steps {
			   bat 'mvn clean deploy -DmuleDeploy -Duser=Shubh_123 -Dpass=Shubh@123'
			}
		}
    }
	
}