pipeline {
    agent {label 'java'}
    parameters {
        choice(name: 'choices', choices: ['one', 'two'])
    }
    stages {
        stage('clone step') {
            steps {
      sh 'rm -rf hello-world-war' 
             sh 'git clone https://github.com/samarthgowda85/hello-world-war.git'
            }
        }
        stage('build step') {
            steps{
            sh 'mvn package'
    }
}
        stage('deploy step') {
            steps{
        
                sh 'sudo cp /var/lib/jenkins/workspace/jfrog1/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.64/webapps/'
            }
        }
            }
        }


