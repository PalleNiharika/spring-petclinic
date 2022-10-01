pipeline {
    agent any
     parameters {
        choice(name: 'BRANCH_TO_BUILD', choices: ['branch_1', 'main'], description: 'Branch to build')
        string(name: 'MAVEN_GOAL', defaultValue: 'package', description: 'maven goal')

    }
    stages {
        stage('vcs') {
            steps {
                git branch: 'branch_1', url: 'https://github.com/PalleNiharika/spring-petclinic.git'
            }

        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('archive results') {
            steps {
                junit '**/surefire-reports/*.xml'
            }
        }
    }

}