pipeline{
  agent any
  stages{
      stage('Build'){
        steps{
          sh 'g++ ./main/PES1UG20CS438.cpp'
          build job : 'PES1UG20CS438-1'
        }
      }
      stage('Test'){
        steps{
          sh './a.out'
          echo 'Test Stage Successful'
        }
      }
      stage('Deploy'){
        steps{
          echo 'Deployed'
        }
      }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}    
