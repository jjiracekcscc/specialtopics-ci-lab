
node {
  try {
    stage('checkout sources') {
          // You should change this to be the appropriate thing
          git url: 'https://github.com/jjiracekcscc/specialtopics-ci-lab'
    }

    stage('Build') {
      // you should build this repo with a maven build step here
      steps {
          withMaven (maven: 'maven3') {
              sh "mvn clean"
              sh "mvn package"
          }
      }
      echo "hello"
    }
  }
  finally {
      junit 'target/**/*.xml'
  }

}
