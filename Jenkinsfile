pipeline{
  agent any
  stages('Build'){
    steps{
      sh 'g++ shashank.cpp -o PES1UG20CS395'
      echo 'Build Successfull'
    }
  }
  stages('Test'){
    steps{
      sh './PES1UG20CS395'
    }
  }
  stages('Deploy'){
    steps{
      sh 'mvn deploy'
      echo 'Deploy Success'
    }
  }
  post{
    failure{
      echo 'Build Failed!'
    }
  }
}
