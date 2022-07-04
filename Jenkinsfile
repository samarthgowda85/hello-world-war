pipeline {
    agent any
    stages {
        stage('clone step') {
            steps {
      sh 'rm -rf hello-world-war' 
             sh 'git clone https://github.com/samarthgowda85/hello-world-war.git'
            }
        }
        stage('build step') {
            sh 'mvn package'
    }
}        
}
}
