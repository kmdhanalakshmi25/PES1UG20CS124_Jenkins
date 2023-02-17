pipeline{
  agent any
  
  stages{
    stages('Build'){
      steps{
        sh 'g++ -o hello pes1ug20cs124.cpp'
        build job:PES1UG20CS124-1
      }
    }
    stage('Test'){
      steps{
        sh './pes1ug20cs124'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deployed successfully'
      }
    }
  }
  post{
    always{
      script{
        if(currentBuild.result == 'FAILURE'){
          echo 'pipeline failed'
        }
      }
    }
  }
}
