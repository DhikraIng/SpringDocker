pipeline {
  agent any
  environment {
    registryBack = "dhikrah/spring-docker-project"
    registryCredential = 'docker-hub'
    customDockerSpringImage = '' 
    latestDockerSpringImage = '' 
  }
  stages {

    
 
    stage('Build Spring Image') {
      steps {
        script {
           latestDockerSpringImage = docker.build(env.registryBack)
         }
      }
    }

    stage('Deploy Spring Image') {
      steps {
        script {

          docker.withRegistry('https://registry.hub.docker.com', env.registryCredential) {
			latestDockerSpringImage.push("$BUILD_NUMBER")
			latestDockerSpringImage.push('latest')          
		
		    }
        }
      }
    }
stage('Deployyyy') {
      bat "D:\jenk.bat" 
 
}
 
  }
}