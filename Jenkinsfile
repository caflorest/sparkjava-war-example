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
              docker cp "/root/workspace/Pipeline_CarlosF/target/sparkjava-hello-world-1.0.war"  elegant_chandrasekhar:"/usr/local/tomcat/webapps"
                '''
            }
        }
    }
}
