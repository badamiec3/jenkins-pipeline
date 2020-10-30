pipeline {
  agent any
  environment{
      DB_PASSWORD=credentials('DATABASE_PASSWORD')
  }
  stages{
    stage('Make Python Script') {
      steps {

      sh 'chmod a+x ./scripts/make-python.sh' 
      sh ". ./scripts/make-python.sh"
      }
    }
    stage('Run Python Script') {
      steps {
    // Run the script with Python3
      sh 'python3 helloworld.py'
      }
    }
     stage('Create Files') {
      steps {
      sh "mkdir ~/jenkins-tutorial-test"
      sh "touch ~/jenkins-tutorial-test/file1 ~/jenkins-tutorial-test/file2"
      }
    }
    stage('show password') {
      steps {
        sh "echo ${DB_PASSWORD}" 
      }
    }
  }

}
