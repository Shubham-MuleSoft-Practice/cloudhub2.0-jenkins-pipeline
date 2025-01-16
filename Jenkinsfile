pipeline
{
	agent any
	stages{
		stage('Build Application') {
			steps {
			   bat 'mvn clean deploy -U -Dlog4j2.loggerContextFactory=org.apache.logging.log4j.simple.SimpleLoggerContextFactory -Dmunit.failIfNoTests=false -s C:\\Users\\Admin\\.m2\\settings.xml'
		   }
	    }
		  stage('Run MUnit Tests') {
            steps {
                echo '***** Running MUnit test cases *****'
                bat 'mvn clean test -DskipVerification=true -s C:\\Users\\Admin\\.m2\\settings.xml'
            }
        }
		stage('Deploy CloudHub 2.0') {
			steps {
			   bat 'mvn clean deploy -DmuleDeploy -Duser=Shubh_123 -Dpass=Shubh@123 -X'
			}
		}
    }
	
}