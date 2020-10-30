pipeline {
  agent any
  stages{
    stage('Make Python Script') {
      // Make the file
      sh 'touch helloworld.py'
      // Put concent in file
      sh 'echo "print('hello world')" > helloworld.py'
    }
    stage('run python script') {
    // Run the script with Python3
      python3 helloworld.py
    }
  }

}
