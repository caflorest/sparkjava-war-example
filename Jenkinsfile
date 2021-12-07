pipeline {
    agent {node {label "CarlosF"}}
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
              docker cp "/root/sparkjava-war-example/target/sparkjava-hello-world-1.0.war" thirsty_murdock:"/usr/local/tomcat/webapps"
                '''
            }
        }
    }
}
