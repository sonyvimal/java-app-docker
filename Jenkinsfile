echo "GIT Repository - Java Project"

node {
  stage('GITHub Repository Codebase Checkout'){
    git 'https://github.com/sonyvimal/java-app'
  }
  stage('Package Compilation'){
    sh 'mvn package'
  }
  stage('Email Notification'){
    mail bcc: '', body: '''This is local Jenkins | Build Reports
    Thanks - GTA''', cc: '', from: '', replyTo: '', subject: 'From Jenkins Server | Local System', to: 'vimal.soni@gta-travel.com'
  }
}
