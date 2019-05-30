node{
    stage ('Codebase checkout'){
        git credentialsId: 'github-credentials', url: 'https://github.com/sonyvimal/java-app-docker'
    }
    stage ('Build Maven Package'){
        def mavenHome = tool name: 'M3', type: 'maven'
        def mavenCommand = "${mavenHome}/bin/mvn"
        sh label: '', script: "${mavenCommand} clean package"    
    }
}
