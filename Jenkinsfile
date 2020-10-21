node{
    def mvnHome
	           stage('Preparation') {
       git 'https://github.com/amar5607/sonar_jenkins_testing.git'
	         mvnHome = tool 'maven_new'
	                                 }
           stage('SonarQube Analysis') {
                                    withSonarQubeEnv('sonar') { 
                                  sh "${mvnHome}/bin/mvn clean sonar:sonar"
                                    }
									}
}
