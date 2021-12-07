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
                mvn clear install
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
