pipeline {
  agent {
    label 'JenkinsSlave'
  }
  stages {
    stage ('SCM') {
      steps {
        echo "Git Checkout"
        git 'https://github.com/DineshPazhaniyandi/StaticApp.git'
      }
    }
    stage ('Validation') {
      steps {
        echo "Build and Test"
      }
    }
    
    stage ('Deploy Stage') {
      steps {
        echo "Deploy"
        sh label: '', script: 'chmod 777 /home/ubuntu/workspace/StaticHtmlProject/deployWeb.sh'
        sh label: '', script: '/home/ubuntu/workspace/StaticHtmlProject/deployWeb.sh'
      }
    }
  }
}
