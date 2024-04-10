pipeline {
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('Git Check out') {
              steps{
                  checkout scm
              }
    }

    stage('Build avec Maven') {
      steps {
        sh "${mvn}/bin/mvn clean package"
      }
    }
    
     

        stage('Package') {
            steps {
                // Package the project
                sh 'mvn package'
            }
        }
    }
}
