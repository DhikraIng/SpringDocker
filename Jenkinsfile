pipeline {
  agent any
  environment {
    registryBack = "dhikrah/spring-docker-project"
    registryCredential = 'docker-hub'
    customDockerSpringImage = '' 
    latestDockerSpringImage = '' 
  }
  stages {

    
  
    stage('Pull image ') {
      steps {
        script {
		sh '''#!/bin/bash
                docker pull dhikrah/spring-docker-project:latest
         '''
       
        }
      }
    }

  }
}