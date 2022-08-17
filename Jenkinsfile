pipeline {

  agent any

  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "** Munit test cases **"
      }
    }

    stage('Deployment') {
      steps {
            bat 'mvn -U -V -e -B -DskipTests -PDev deploy -DmuleDeploy'
      }
    }
  }
}