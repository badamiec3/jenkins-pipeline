pipeline {
  agent any
  stages{
    stage('Make Python Script') {
      steps {
      // Make the file
      sh 'touch helloworld.py'
      // Put concent in file
      sh echo 'print("hello world")' > helloworld.py
      sh 'chmod a+x ./scripts/make-python.sh' 
      sh "./scripts/make-python.sh"
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
