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
  stage('Slack Notification'){
    slackSend baseUrl: 'https://hooks.slack.com/services/',
    channel: '#gta', color: 'good',
    message: 'Jenkins Notification',
    teamDomain: 'devops-lcc7986.slack.com',
    tokenCredentialId: 'slack-demo'
  }
}
