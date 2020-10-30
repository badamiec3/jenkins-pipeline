pipeline {
  agent any
  stages{
    stage('Make Python Script') {
      steps {

      sh 'chmod a+x ./scripts/make-python.sh' 
      sh ". ./scripts/make-python.sh"
      }
    }
    stage('run python script') {
      steps {
    // Run the script with Python3
      sh 'python3 helloworld.py'
      }
    }
  }

}
