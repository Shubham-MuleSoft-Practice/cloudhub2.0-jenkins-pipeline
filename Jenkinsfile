pipeline
{
	agent any
	stages{
		stage('Build Application') {
			steps {
			   bat 'mvn clean deploy -U -s C:\\Users\\Admin\\.m2\\settings.xml'
		   }
	    }
		  stage('Run MUnit Tests') {
            steps {
                echo '***** Running MUnit test cases *****'
                bat 'mvn clean test -Dmunit.failIfNoTests=false C:\\Users\\Admin\\.m2\\settings.xml'
            }
        }
		stage('Deploy CloudHub 2.0') {
			steps {
			   bat 'mvn clean deploy -DmuleDeploy -Duser=Shubh_123 -Dpass=Shubh@123 -X'
			}
		}
    }
	
}