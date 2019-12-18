pipeline {
  agent {
    label 'JenkinsSlave'
  }
  stages {
    stage ('SCM') {
      steps {
        echo "Git Checkout"
        git 'https://github.com/RajivKumarVA/JenkinsProj.git'
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
        sh label: '', script: 'chmod 777 /home/ubuntu/workspace/Pipeline-Lab-Project/deployWeb.sh'
        sh label: '', script: '/home/ubuntu/workspace/Pipeline-Lab-Project/deployWeb.sh'
      }
    }
  }
}
