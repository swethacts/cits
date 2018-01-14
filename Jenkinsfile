pipeline {
  agent any
  stages {
    stage('Version') {
      agent { docker 'atin/cits' } 
      steps {
        sh 'echo "helloworld"'
        sh 'pwd'
        sh 'ls -ltr'
        sh 'chmod 777 run.sh'
        //sh 'chmod 777 Run.command'
        sh './run.sh -run -project_location “./Projects/DemoProject” -release “eCommerce” -testset “Cycle1”'
        //sh './Run.command -run -project_location “./Projects/DemoProject” -release “eCommerce” -testset “Cycle1”'
      }
    }
  }
}
