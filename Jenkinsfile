pipeline{
  agent{
    docker{
      image 'python:3.11-slim'
    }
  }

  
  stages{
    stage('show environment'){
      steps{
        sh 'python --version'
        sh 'pwd'
        sh 'ls -la'
      }
      
    }
    stage('install dependencies'){
      steps{
        sh 'pip install --no-cache-dir -r requirements.txt'
      }
      
    }
    stage('run tests'){
      steps{
        sh 'pytest test_calculator.py -v'
      }
      
    }
    stage('run calculator'){
      steps{
        sh 'python calculator.py'
      }
    }

    
  }
}
