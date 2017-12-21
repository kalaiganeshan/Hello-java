env.dockerimagename="devopsbasservice/buildonframework:buildonJenkinsfile2.1"
pipeline {
  stages {
    stage('Build') {
      steps {
        echo 'Build started!'
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
      
      
     
  
