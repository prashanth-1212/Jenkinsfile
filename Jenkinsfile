node
{
properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '5')), pipelineTriggers([pollSCM('* * * * *')])])
  echo "GitHub BranhName ${env.BRANCH_NAME}"
      echo "Jenkins Job Number ${env.BUILD_NUMBER}"
      echo "Jenkins Node Name ${env.NODE_NAME}"
  
      echo "Jenkins Home ${env.JENKINS_HOME}"
      echo "Jenkins URL ${env.JENKINS_URL}"
      echo "JOB Name ${env.JOB_NAME}"

stage('pulling project from git hub')
{
git branch: 'development', credentialsId: 'ee61430e-1b31-4942-9883-86cc2183c8ca', url: 'https://github.com/prashanth-1212/maven-web-application.git'
}
stage('build project')
{
sh "mvn clean package"
}
}
