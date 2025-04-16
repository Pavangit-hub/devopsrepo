pipeline {
  agent any

  environment {
    APP_NAME = "MyApp"
  }

  stages {
    stage('Checkout') {
      steps {
        git url: 'https://github.com/Pavangit-hub/https://github.com/Pavangit-hub/devopsrepo.git.git', credentialsId: 'github-token'
      }
    }

    stage('Build') {
      steps {
        sh '''
          echo "Building $APP_NAME"
          # Add your build script or commands here
        '''
      }
    }

    stage('Deploy') {
      steps {
        sh '''
          echo "Deploying $APP_NAME"
          # Add your deployment script here
        '''
      }
    }
  }

  post {
    success {
      echo 'Pipeline completed successfully!'
    }
    failure {
      echo 'Pipeline failed.'
    }
  }
}
