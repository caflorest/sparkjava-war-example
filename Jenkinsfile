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
                echo "hola"
                '''
            }
        }
    }
}
