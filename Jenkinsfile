pipeline{
  agent any
  stages {
    stage('Deploy') {
	  environment {
    //adding a comment for the commit test
		ANYPOINT_CREDENTIALS = credentials('bookMyHoliday')
  }
      steps {
        bat 'mvn clean package deploy -DmuleDeploy -Dusername="%ANYPOINT_CREDENTIALS_USR%" -Dpassword="%ANYPOINT_CREDENTIALS_PSW%" -Denvironment=Sandbox -Dregion=us-east-2 -Dworkers=1 -DworkerType=MICRO'
      }
    }
  }
}