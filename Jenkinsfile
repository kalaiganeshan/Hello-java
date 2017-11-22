pipeline {
 agent {
        label {
            label ""
            customWorkspace ${JOB_NAME}/${CUSTOM_BUILD_PARAM}/${BUILD_NUMBER}
        }
    }

  stages {
    stage('Build') {
      steps {
        echo 'Build started!'
        sh 'mvn clean package -DskipTests=true'
      }
    }
    stage('Test') {
      parallel {
        stage('Unit Tests') {
          steps {
            echo 'Unit Tests Are Awesome!'
          }
        }
        stage('Integration Tests') {
          steps {
            echo 'Integration Tests Are Awesome!'
          }
        }
        stage('Smoke Tests') {
          steps {
            echo 'Where There is Smoke there is Fire!!!'
          }
        }
        stage('Reg Test') {
          steps {
            echo 'Reg Test executed'
          }
        }
      }
    }
   /* stage('CodeAnalysis') {
      steps {
        echo '-----Sonar Analysis started----'
        sh 'mvn sonar:sonar -Dsonar.host.url=http://54.89.101.39:9000/sonar/ -Dsonar.sources=src/main/java'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Ship It!'
        sh 'mvn deploy:deploy-file -DgroupId=org.blueocean.samples -DartifactId=blueocean-hello-java -Dversion=1.0 -DgeneratePom=true -Dpackaging=war -DrepositoryId=nexus -Durl=http://54.89.101.39:8082/repository/studiorepo -Dfile=target/blueocean-hello-java-1.0.war'
      }
    } */
  }
}
