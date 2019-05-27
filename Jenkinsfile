echo "GIT Repository - Java Project"

node {
  stage('GITHub Repository Codebase Checkout'){
    git 'https://github.com/sonyvimal/java-app'
  }
  stage('Package Compilation'){
    sh 'mvn package'
  }
}
