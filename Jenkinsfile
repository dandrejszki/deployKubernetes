pipeline {

  agent { label 'kubepods' }

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/dandrejszki/deployKubernetes.git'
      }
    }
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "hello-depl.yaml", kubeconfigId: "kubeconfigJenkins")
        }
      }
    }

  }

}
