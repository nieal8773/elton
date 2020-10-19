pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        echo 'This is $BUID_NUMBER in demo $DEMO'
        sh 'echo "This is build $BUILD_NUMBER in demo $DEMO"'
      }
    }

  }
}