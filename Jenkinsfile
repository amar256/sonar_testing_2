node {
  def mvnHome
  stage('SCM') {
    git 'https://github.com/amar5607/sonar_testing_2.git'
	mvnHome = tool 'maven_new'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv('sonar_qube') {
      sh 'sh 'sonar-scanner'
    } // submitted SonarQube taskId is automatically attached to the pipeline context
  }
}
 
