pipeline {
  agent any
  stages {
    stage('Version') {
      steps {
        sh 'echo "helloworld"'
        sh 'pwd'
        sh 'ls -ltr'
        sh './run.sh -run -project_location “./Projects/DemoProject” -release “eCommerce” -testset “Cycle1”'
      }
    }
  }
}
