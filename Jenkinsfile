pipeline {
     agent any
      stages {
            stage('Clone Repo') {
                  steps {
	     echo 'Cloning the Repository'
	     git branch:'main',url:'https://github.com/bhavyashreeguna08/cdacRepo.git',credentialsId:'git.cred'
	 }
            }
             stage('Build') {
	  steps {
	     echo 'Building the application'
                      bat 'first.bat'
	 }

            }
            stage('Test') {
	  steps {
	     echo 'Running the test cases'
                      bat 'echo "All Tests Passed"' 
	 }

            }
            stage('Deploy') {
	  steps {
	     echo 'Deploying the application'
	     bat 'echo "Deployment Successfull"' 
	 }
}
      }
            post{
	always{
           	     echo 'Pipeline execution Completed' 
                 }
             }

     
}
