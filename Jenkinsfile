node{
    def mvnHome
	           stage('Preparation') {
       git 'https://github.com/amar5607/sonar_testing_2.git'
	         mvnHome = tool 'maven_new'
	                                 }
           stage('SonarQube Analysis') {
                                    withSonarQubeEnv('sonar') { 
                                  sh "${mvnHome}/bin/mvn clean package sonar:sonar"
                                    }
									}
}
