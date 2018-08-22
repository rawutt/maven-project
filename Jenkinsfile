pipeline {
    agent any

    tools {
        maven 'localMaven'
    }
    
   /* parameters {
        string(name: 'tomcat_dev', defaultValue: '34.253.226.73', description: 'Staging Server')
        string(name: 'tomcat_prod', defaultValue: '52.212.38.156', description: 'Production Server')
    } */

stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}
