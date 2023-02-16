pipeline{
  agent any
  stages{
    stage('Build'){
    steps{
      sh 'g++ shashank.cpp -o PES1UG20CS395'
      echo 'Build Successfull'
    }
  }
  stage('Test'){
    steps{
      sh './PES1UG20CS395'
    }
  }
  stage('Deploy'){
    steps{
      sh 'mvn deploy'
      echo 'Deploy Success'
    }
  }
  }
  post{
    failure{
      echo 'Build Failed!'
    }
  }
  
}
