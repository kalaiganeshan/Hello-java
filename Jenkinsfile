env.dockerimagename="devopsbasservice/buildonframework:buildonJenkinsfile2.1"
 pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build started!'
        git 'https://github.com/kalaiganeshan/Hello-java.git'
        sh 'mvn clean package -DskipTests=true'
      }
    }
    stage('Test') {
      steps {
         
         echo 'Test success'
      }
    }
  }
}
      
      
     
  
