pipeline {
    agent any
    stages {
        stage('vcs') {
            steps {
                git branch: 'branch_1', url: 'https://github.com/PalleNiharika/spring-petclinic.git'
            }

        }
        stage('build') {
            steps {
                mvn package
            }
        }
        stage('archive results') {
            steps {
                junit '**/surefire-reports/*.xml'
            }
        }
    }

}