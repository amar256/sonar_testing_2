node{
    def mvnHome
	def workspace
	           stage('Preparation') {
       git 'https://github.com/amar5607/sonar_jenkins_testing.git'
	         mvnHome = tool 'maven_new'
			 scannerhome = tool 'sonar'
	                                 }
           stage('SonarQube Analysis'){
		   sh """echo ${workspace}"""
                                    withSonarQubeEnv('sonar') { 
                                     sh """${scannerhome}/bin/sonar-scanner -D sonar.projectKey=jenkins sonar.sources=src/main"""
                                    }
									}
}
