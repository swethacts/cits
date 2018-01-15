pipeline {
  agent any
  stages {
    stage('Version') {
      agent { docker 'atin/cits' } 
      steps {
		slackSend color: "2187e0", message: "`Creating CITS Docker container...`"
		slackSend color: "2187e0", message: "`Starting Functional Test Execution. Job Details: ${env.JOB_NAME} ${env.BUILD_NUMBER}` (<${env.BUILD_URL}|Open>)"
        
		sh '''
			echo "Starting test execution.."        
		    pwd
			ls -ltr
			chmod 777 run.sh
			./run.sh -run -project_location “./Projects/DemoProject” -release “eCommerce” -testset “Cycle1”
		'''
		slackSend color: "e50b0b", message: "`Functional Test Execution Complete. Job URL:` (<${env.BUILD_URL}|Open>)"
		slackSend color: "67bc73", message: "`Destroying Docker container...`"
		
        //sh 'chmod 777 Run.command'
        //sh './Run.command -run -project_location “./Projects/DemoProject” -release “eCommerce” -testset “Cycle1”'
      }
    }
  }
}
