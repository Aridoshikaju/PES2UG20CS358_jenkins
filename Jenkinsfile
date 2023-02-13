pipeline{
  agent any
  stages{
  stage('Build') {
    steps{
      sh 'g++ -o making_error PES2UG20CS358.cpp'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS000'
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL'
    }
  }
  }

  post {
    failure {
        echo 'Pipeline Failed'
    }
  }
}
