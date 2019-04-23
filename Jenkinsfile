pipeline {
  agent { label 'node1'}
  stages {
   stage("checkout"){
    steps {
      git "https://github.com/sairamkodipyaka/myProject.git"
    }
   }
   stage('build') {
     steps {
       sh 'mvn clean compile'
     }
   }
   stage('Test') {
     steps {
       sh 'mvn test'
       junit '**/target/surefire-reports/Test-8.xml'
     }
   }
   stage('Package') {
     steps {
       sh 'mvn package'
     }
   }
  }
}
