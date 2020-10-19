pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      environment {
        LOG_LEVEL = 'INFO'
      }
      steps {
        echo "Building release $RELEASE with log Level $LOG_LEVEL"
      }
    }

    stage('Test') {
      steps {
        echo "Testing. I can see release $RELEASE"
      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Deploy?', submitter: 'name', ok: 'Do it!', submitterParameter: 'TARGET_ENVIRONMENT')
        echo "Deploying release $RELEASE to environment $TARGET_ENVIRONMENT"
      }
    }

  }
  environment {
    RELEASE = '20.04'
  }
}
