node('OPENJDK-11-MVN') {
    stage('vcs') {
    git branch: 'branch_1', url: 'https://github.com/PalleNiharika/spring-petclinic.git'
}
    stage('build') {
    sh '/opt/apache-maven-3.8.6/bin/mvn package'
}
stage('archive results') {
  junit '**/surefire-reports/*.xml'
}
}
 