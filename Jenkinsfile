pipeline {
    agent {node {label "CFD2"}}
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                '''
            }
        }
 stage("build") {
            steps {
                sh '''
                mvn clean install
                '''
            }
        }
 stage("Deploy") {
            steps {
                sh '''
              docker cp "/root/workspace/d2_Pipeline_multibranchCF_Ingles/target/sparkjava-hello-world-1.0.war"  tomcat_ing:"/usr/local/tomcat/webapps"
              
              
                '''
            }
        }
    }
}
