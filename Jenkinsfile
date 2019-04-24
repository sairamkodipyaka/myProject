pipeline {
  agent { label 'node1'}
  tools { maven 'Maven'}
  stages {
   stage("checkout"){
    steps {
      git "https://github.com/sairamkodipyaka/myProject.git"
    }
   }
   stage('build') {
     steps {
       bat 'mvn clean compile'
     }
   }
   stage('Test') {
     steps {
       bat 'mvn test'
       junit '**/target/surefire-reports/Test-8.xml'
     }
   }
   stage('Package') {
     steps {
       bat 'mvn package'
     }
   }
  }
}
