pipeline {
    agent any
    
    environment{
        PATH = "/opt/maven/bin:$PATH"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sappidi341/hello-world']]])
            }
        }
        
        stage('build') {
            steps {
               sh "mvn clean install" 
            }
        }
    }
}
