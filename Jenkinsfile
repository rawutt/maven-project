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
            }
          /*  post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            } */
        }

   /*     stage ('Deployments'){
            parallel{
                stage ('Deploy to Staging'){
                    steps {
                        sh "scp -i /home/jenkins/tomcat-demo.pem **/target/*.war ec2-user@${params.tomcat_dev}:/var/lib/tomcat7/webapps"
                    }
                }

                stage ("Deploy to Production"){
                    steps {
                        sh "scp -i /home/jenkins/tomcat-demo.pem **/target/*.war ec2-user@${params.tomcat_prod}:/var/lib/tomcat7/webapps"
                    }
                }
            }
        } */
    }
}
