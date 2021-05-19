pipeline {
  agent any
  environment {
    registryBack = "dhikrah/spring-docker-project"
    registryCredential = 'docker-hub'
    customDockerSpringImage = '' 
    latestDockerSpringImage = '' 
  }
  stages {

    
  
        stage ('Hello Test stage') {
            agent any

            steps {
                echo 'Hello, '

                sh '''#!/bin/bash

                    echo "Hello from bash"
                    echo "Who I'm $SHELL"
                '''
            }
        }
    stage('Pull image ') {
      steps {
        script {
		echo 'Hellosss, '

                sh ''' 
				docker pull dhikrah/spring-docker-project:latest
                '''
		 
       
       
        }
      }
    }

  }
}